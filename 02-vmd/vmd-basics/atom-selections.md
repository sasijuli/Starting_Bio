# Atom Selections In VMD

## Goal

Learn how VMD selects atoms for visualization and analysis.

## Why Atom Selections Matter

Most useful VMD workflows depend on selecting a specific part of a molecular system. A selection can represent an entire protein, one residue, a ligand, nearby water molecules, a membrane leaflet, or atoms near another selection.

Atom selections are used in two places:

- The graphical interface, especially `Graphics > Representations`
- Tcl scripts, especially with the `atomselect` command

## Selection Examples

```text
all
protein
water
resname LYS
resid 1
name CA
not water
water and within 3 of protein
(resname LYS) or (resname GLY)
```

## Tutorial Notes

Start with simple selections before combining conditions. For example:

1. Type `protein` in the `Selected Atoms` field and apply it.
2. Change the drawing method to `NewCartoon`.
3. Create a new representation.
4. Type `water` and apply it.
5. Create another representation.
6. Type `water and within 3 of protein` and apply it.

The important idea is that the selection controls what VMD draws or analyzes. The drawing method and coloring method only affect how that selected set is displayed.

## Tcl Version

In Tcl, `atomselect` creates a selection object:

```tcl
set sel [atomselect top "protein"]
$sel num
$sel get name
$sel get {resid resname name}
$sel delete
```

For trajectories, a selection can be tied to a frame:

```tcl
set sel [atomselect top "water and within 3 of protein" frame 0]
```

If a selection depends on coordinates, such as `within 3 of protein`, update it when the frame changes:

```tcl
$sel frame 20
$sel update
```

## Practice

Create representations for:

- The full protein
- Lysine residues
- Water within 3 Angstroms of the protein
- Alpha carbons only

Then write the same selections as Tcl `atomselect` commands.

## External References

- VMD `atomselect` command reference: https://www.ks.uiuc.edu/Research/vmd/vmd-1.7.1/ug/node108.html
- VMD molecular analysis section, using `atomselect`: https://www.ks.uiuc.edu/Research/vmd/vmd-1.7.1/ug/node181.html
- Official VMD tutorial, Working with a Single Molecule: https://www.ks.uiuc.edu/Training/Tutorials/vmd/tutorial-html/node2.html
