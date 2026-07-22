# How Can I Analyze A Trajectory Reproducibly?

## Scientific Question

How can I measure structural change across a molecular dynamics trajectory without mixing up frames, selections, alignment, or periodic boundary conditions?

## When To Use This Module

Use this workflow after visual inspection shows a possible trend, such as a domain opening, ligand movement, helix bending, protein compactness change, or altered hydrogen-bond pattern.

## Required Background

- You can load a structure and trajectory into the same molecule.
- You can make stable atom selections.
- You can use `measure` commands and save output from Tcl.
- You know which frames belong to equilibration and which belong to production analysis.

## Analysis Questions

### What part of the trajectory should I analyze?

Decide the first frame, last frame, and step before running analysis. For long trajectories, start with a stride such as every 10th or 100th frame, then increase detail only if needed.

### Do I need to align the trajectory?

Use alignment when measuring internal structural changes. A common strategy is to align protein backbone or alpha carbons to a reference frame, then measure RMSD, distances, or ligand movement after global translation and rotation have been removed.

### Which measurements answer my scientific question?

- **RMSD**: overall structural change relative to a reference.
- **RMSF**: per-atom or per-residue flexibility across frames.
- **Radius of gyration**: compactness of a selection.
- **Distances or angles**: motion between chosen structural features.
- **Contacts and hydrogen bonds**: interaction persistence.
- **Updated selections**: water, ions, or nearby atoms that change over time.

### How do I avoid trajectory-selection errors?

Print selection counts, update coordinate-dependent selections, and use explicit frame ranges. Avoid relying on the current active frame unless the analysis is intentionally interactive.

### How should I handle periodic boundary conditions?

Check whether the molecule, membrane, solvent, or ligand has been split by periodic wrapping before measuring distances, centers, thickness, or diffusion-like quantities. Use a small visual test first, then document the wrapping command, frame range, compound definition, and centering selection. qwrap can be useful when a VMD workflow needs faster wrapping or unwrapping, while PBCTools remains a more general reference point.

## Example Output Table

```text
# frame rmsd rgyr distance_A_B
0 0.000 18.42 7.31
10 0.834 18.55 7.88
20 1.102 18.61 8.24
```

## Validation Checks

- Plot each time series before interpreting it.
- Inspect frames at the beginning, middle, and end of the analysis range.
- Confirm that trajectory visualization uses updated selections when needed.
- Check whether periodic boundary conditions split the molecule or move atoms across cell boundaries.
- Repeat a small part of the result manually in the GUI for sanity checking.

## Expected Output

A documented trajectory workflow with input files, selected frame range, selections, alignment choice, exported data files, and plots.

## Limitations

One metric rarely proves a molecular interpretation by itself. Combine complementary measurements, such as RMSD plus distances or hydrogen bonds plus contact frequency.

## External References

- VMD `measure` command reference, version 1.8.6: https://www.ks.uiuc.edu/Research/vmd/vmd-1.8.6/ug/node124.html
- VMD `atomselect` command reference: https://www.ks.uiuc.edu/Research/vmd/vmd-1.7.1/ug/node108.html
- Official Using VMD tutorial, Trajectories and Movie Making: https://www.ks.uiuc.edu/Training/Tutorials/vmd/tutorial-html/node3.html
- VMD Images and Movies tutorial, Working With Trajectories: https://www.ks.uiuc.edu/Training/Tutorials/vmd-imgmv/imgmv/tutorial-html/node3.html
- qwrap, fast PBC wrapping and unwrapping for VMD: https://github.com/jhenin/qwrap
- Community PBC wrapping discussion for VMD: https://www.researchgate.net/post/how_to_use_pbc_wrap_command_in_vmd_to_re-center_a_multimeric_protein
- Current VMD User's Guide: https://www.ks.uiuc.edu/Research/vmd/current/ug.pdf
