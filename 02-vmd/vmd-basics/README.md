# VMD Basics

## Learning Goals

By the end of this module, you should be able to:

- Explain what VMD is used for
- Load a molecular structure into VMD
- Change molecular representations
- Understand the basics of trajectory visualization
- Select atoms using VMD selection language
- Run basic measurements and analyses
- Use external VMD tutorials as follow-up practice

These skills are prerequisites for the specialized workflows in [VMD Pro](../vmd-pro/).

## Core Ideas

VMD stands for Visual Molecular Dynamics. It is commonly used to visualize biomolecules, inspect structural files, view simulation trajectories, and perform molecular analysis.

## Common File Types

- `.pdb`: Protein Data Bank structure file
- `.psf`: Protein structure file used by CHARMM/NAMD workflows
- `.dcd`: Trajectory file often produced by NAMD

## Suggested Order

1. [Installation](installation.md)
2. [Molecular Visualization In VMD](visualization.md)
3. [Atom Selections](atom-selections.md)
4. [Tcl Scripting In VMD](tcl-scripting.md)
5. [Measurements And Analysis](measurements.md)
6. [Analysis In VMD](analysis.md)
7. [Trajectories And Movies](trajectories-and-movies.md)
8. [Using External VMD Tutorials](tutorial-resources.md)
9. Optional: [VMD Supplementary Link Summaries](../link_summaries.md) for extra practice links and video notes

## Basic Topic Map

- **Install and open VMD**: confirm that VMD starts and that the Main, OpenGL Display, and Console windows are available.
- **Load molecular data**: open a structure file first, then add trajectory files to the same molecule when needed.
- **Build representations**: combine selected atoms, drawing method, coloring method, and material.
- **Select atoms intentionally**: use the same selection language in the graphical interface and Tcl scripts.
- **Measure structures**: start with GUI pick modes for distances, angles, and dihedrals, then reproduce useful values with Tcl.
- **Inspect trajectories**: use playback, smoothing, multiple-frame display, and updated coordinate-dependent selections.
- **Use external tutorials**: practice with official VMD tutorials and use supplementary links as optional reinforcement.

## Practice

1. Download a small protein structure from the Protein Data Bank.
2. Open the structure in VMD.
3. Change the molecular representation.
4. Save a screenshot for your notes.
5. Create one atom selection and use it in a representation.
6. Measure one distance, one angle, and one dihedral.

## External References

- Complete VMD Basics reference list: [references.md](references.md)
- VMD main page: https://www.ks.uiuc.edu/Research/vmd/
- VMD User's Guide: https://www.ks.uiuc.edu/Research/vmd/vmd-new/ug.pdf
- Current VMD User's Guide: https://www.ks.uiuc.edu/Research/vmd/current/ug.pdf
- VMD tutorials: https://www.ks.uiuc.edu/Training/Tutorials/
- VMD tutorial PDF: https://www.ks.uiuc.edu/Training/Tutorials/vmd/vmd-tutorial.pdf
- VMD tutorial HTML: https://www.ks.uiuc.edu/Training/Tutorials/vmd/tutorial-html/index.html
- VMD supplementary link summaries: [link_summaries.md](../link_summaries.md)

## Next Step

After completing these pages, return to the [VMD module overview](../README.md) or continue to [VMD Pro](../vmd-pro/).
