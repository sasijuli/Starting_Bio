# Molecular Visualization In VMD

## Goal

Learn how to display a molecule clearly in VMD.

## Topics

- Loading a molecule
- Changing drawing methods
- Coloring atoms and residues
- Showing protein secondary structure
- Saving images
- Creating multiple representations
- Combining selection, drawing style, coloring method, and material

## Representation Workflow

In VMD, a molecular representation is controlled by four main choices:

- **Selection**: which atoms are shown
- **Drawing method**: how selected atoms are drawn
- **Coloring method**: how colors are assigned
- **Material**: how lighting, shading, and transparency are applied

A useful beginner workflow is:

1. Load a `.pdb` file.
2. Open `Graphics > Representations`.
3. Start with `Selected Atoms: protein`.
4. Try `Drawing Method: NewCartoon`.
5. Try `Coloring Method: Secondary Structure` or `Structure`.
6. Create a second representation for a specific feature, such as `resname LYS`, `water`, or `within 3 of protein`.

This approach comes from the official VMD tutorial's single-molecule workflow, which uses ubiquitin to practice loading molecules, changing drawing styles, changing coloring methods, and displaying selected parts of a structure.

## Practice

Open a `.pdb` file in VMD and try at least three visual representations:

- Lines
- NewCartoon
- VDW

Write down which representation is most useful for inspecting the full protein structure.

## External References

- Official VMD tutorial, Working with a Single Molecule: https://www.ks.uiuc.edu/Training/Tutorials/vmd/tutorial-html/node2.html
- Current VMD User's Guide: https://www.ks.uiuc.edu/Research/vmd/current/ug.pdf
