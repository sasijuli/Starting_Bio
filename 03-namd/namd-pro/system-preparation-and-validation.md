# How Can I Prepare And Validate A NAMD System?

## Scientific Question

How can I confirm that a structure, topology, parameter set, solvent box, ions, and boundary conditions are consistent before running minimization?

## Required Files

- Coordinate file, usually `.pdb`
- Structure file, usually `.psf`
- Force-field topology and parameter files
- NAMD configuration file
- Notes on residue naming, protonation, ligands, water model, ions, and patches

## Validation Questions

### Do the coordinate and structure files describe the same system?

Check atom counts, segment names, residue names, chain breaks, terminal patches, disulfides, ligands, ions, and waters. Load the system in VMD and inspect suspicious regions before trusting the files.

### What does the PSF file contribute?

The PSF file stores molecule-specific force-field information such as atoms, bonds, angles, dihedrals, impropers, cross-terms, atom types, charges, and masses. NAMD and VMD require the atom order in PDB, DCD, and other coordinate data to match the atom order in the PSF.

### Are the topology and parameter files compatible?

The NAMD tutorial explains that CHARMM parameter files are tied to the topology files used to generate the PSF. Do not mix topology and parameter versions casually. For CHARMM-family workflows, use current CHARMM36/C36m files from the MacKerell site or a documented tool such as CHARMM-GUI.

### Is the water model explicit and supported?

Record whether the system uses TIP3P, TIP4P, TIP4P/2005, or another water model. For uncommon water models, keep example files or tested templates with the project so dummy sites, masses, topology, and parameters are not guessed later.

### Are restraints and fixed atoms documented?

Document every restraint source: fixed atoms, harmonic constraints, extra bonds, rigid bonds, or custom restraint files. These settings affect physical interpretation and may affect pressure calculations.

## Pre-Minimization Checklist

- Load the final `.psf` and `.pdb` in VMD.
- Confirm atom count and residue count.
- Inspect termini, missing atoms, ligand names, waters, and ions.
- Check that every parameter file is listed in the NAMD config.
- Record force-field version and water model.
- Confirm periodic cell vectors and origin.
- Run a short minimization test and inspect the log for missing parameters or bad contacts.

## Expected Output

A documented input bundle containing final coordinates, structure, parameter files, topology files, configuration files, and a completed validation checklist.

## External References

- NAMD tutorial, Unix/MacOSX PDF: https://www.ks.uiuc.edu/Training/Tutorials/namd/namd-tutorial-unix.pdf
- NAMD tutorial, PSF files: https://www.ks.uiuc.edu/Training/Tutorials/namd/namd-tutorial-unix-html/node23.html
- NAMD tutorial, parameter files: https://www.ks.uiuc.edu/Training/Tutorials/namd/namd-tutorial-unix-html/node25.html#:~:text=given%20in%20the%20parameter%20files,/mole/rad**2%20!
- CHARMM force field files, MacKerell Lab: https://mackerell.umaryland.edu/charmm_ff.shtml
- NAMD constraints and restraints: https://www.ks.uiuc.edu/Research/namd/2.13/ug/node27.html
- NAMD-L TIP4P discussion: https://www.ks.uiuc.edu/Research/namd/mailing_list/namd-l.2010-2011/2303.html
- Scalable Molecular Dynamics with NAMD: https://pmc.ncbi.nlm.nih.gov/articles/PMC2486339/
