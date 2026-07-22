# How Can I Analyze Protein-Ligand Interactions?

## Scientific Question

How can I describe which residues interact with a ligand and whether those interactions persist across a trajectory?

## When To Use This Module

Use this workflow for a docked ligand, crystallographic ligand, cofactor, inhibitor, substrate, or small molecule that remains near a protein binding site.

## Required Background

- You can identify the ligand residue name or segment name.
- You can make selections for protein, ligand, and binding-site residues.
- You can measure distances, contacts, and hydrogen bonds.
- You can align a trajectory to the protein or binding site before comparing ligand motion.

## Analysis Questions

### How do I define the ligand?

Start with a selection that is stable and specific:

```text
resname LIG
resname ATP
segname L
not protein and not water and not ions
```

Confirm the ligand atom count with `$ligand num` and visually inspect the selected atoms.

If a ligand, cofactor, or modified residue was manually edited, check atom names and record types against the expected PDB conventions before using the structure for topology generation or analysis.

### How do I define the binding site?

Use a geometric selection for exploration, then convert important residues into a stable list:

```text
protein and within 4 of resname LIG
protein and resid 25 48 91 145
```

The first selection finds nearby residues; the second is easier to reproduce once the important residues are known.

### How do I track contacts over time?

Use distance cutoffs or `measure contacts` between ligand and protein selections. Report contact frequency as a percentage of analyzed frames, and keep the cutoff in the output notes.

### How do I track hydrogen bonds?

Use a hydrogen-bond workflow with clear donor and acceptor selections, cutoff, and angle criteria. Check ambiguous cases manually because atom naming, protonation, missing hydrogens, and shared selections can affect interpretation.

### How do I monitor ligand movement?

Align the protein or binding site, then measure ligand center, key atom distances, orientation vectors, or RMSD relative to the first frame. Avoid aligning on the ligand if the goal is to measure ligand motion relative to the protein.

## Suggested Output

- A binding-site representation showing ligand and nearby residues.
- A table of protein-ligand contacts with residue name, residue id, contact frequency, and minimum distance.
- A plot of one or more important distances across the trajectory.
- Notes listing ligand selection, protein selection, cutoff values, and analyzed frame range.

## Validation Checks

- Confirm that the ligand selection contains only the ligand.
- Inspect the first, middle, and last frames with the same representation.
- Check residue numbering against the original structure.
- Record protonation and missing-hydrogen assumptions before interpreting hydrogen bonds.

## External References

- VMD `measure` command reference, version 1.8.6: https://www.ks.uiuc.edu/Research/vmd/vmd-1.8.6/ug/node124.html
- VMD `atomselect` command reference: https://www.ks.uiuc.edu/Research/vmd/vmd-1.7.1/ug/node108.html
- VMD molecular analysis section, using `atomselect`: https://www.ks.uiuc.edu/Research/vmd/vmd-1.7.1/ug/node181.html
- Compchems guide to VMD distance, angle, and dihedral measurements: https://www.compchems.com/vmd-measurements-analyze-distances-and-angles-with-vmd/#tracking-distance-during-the-simulation
- Molefacture tutorial: https://www.ks.uiuc.edu/Training/Tutorials/vmd-molefacture/tutorial-Molefacture.pdf
- PDB format reference: https://www.biostat.jhsph.edu/~iruczins/teaching/260.655/links/pdbformat.pdf
- Current VMD User's Guide: https://www.ks.uiuc.edu/Research/vmd/current/ug.pdf
