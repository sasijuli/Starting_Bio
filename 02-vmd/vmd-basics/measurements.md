# Measurements In VMD

## Goal

Learn how to measure structural features in VMD using both the graphical interface and Tcl commands.

## What You Can Measure

Common beginner measurements include:

- Distance between two atoms
- Angle across three atoms
- Dihedral angle across four atoms
- Radius of gyration
- RMSD between structures or frames
- Hydrogen bonds
- Contacts between two selections

## GUI Measurements

Use the keyboard pick modes in the VMD Display window:

- `2`: pick two atoms for a distance
- `3`: pick three atoms for an angle
- `4`: pick four atoms for a dihedral

After selecting atoms, VMD displays a label with the measured value. If a trajectory is loaded, the value can change as the frame changes.

To manage labels:

1. Open the Labels window.
2. Select the label type, such as atoms, bonds, angles, or dihedrals.
3. Delete labels that are no longer useful.
4. Plot or save label data when following a measurement across frames.

## Tcl Measurements

For reproducible analysis, use the `measure` command.

```tcl
set protein [atomselect top "protein"]
measure center $protein
measure rgyr $protein
$protein delete
```

For distances, angles, and dihedrals, use atom indices:

```tcl
measure bond {3 5}
measure angle {3 5 8}
measure dihed {3 5 8 12}
```

When working with trajectories, specify frames or frame ranges when appropriate. This is important because the current frame may not be the frame you intended to analyze.

## Beginner Workflow

1. Use the GUI to identify the atoms of interest.
2. Record atom names, residue names, and atom indices.
3. Reproduce the measurement with a Tcl command.
4. Save the command in your notes.
5. If the value changes over a trajectory, save the data and plot it later.

## Practice

Use any small `.pdb` file and complete these tasks:

1. Measure one distance with the GUI.
2. Measure one angle with the GUI.
3. Measure one dihedral with the GUI.
4. Repeat one measurement using Tcl.
5. If a trajectory is loaded, save the distance over all frames.

## Supplementary Tutorial

After completing the exercises above, use the [Compchems VMD measurements guide](https://www.compchems.com/vmd-measurements-analyze-distances-and-angles-with-vmd/#distance-measurements-in-vmd) for another GUI-based example of distances, angles, dihedrals, labels, and trajectory-dependent measurements.

See the local [VMD supplementary link summary](../link_summaries.md#measurements) for guidance on how this resource fits into the tutorial.

## External References

- VMD `measure` command reference, version 1.8.5: https://www.ks.uiuc.edu/Research/vmd/vmd-1.8.5/ug/node124.html
- VMD `measure` command reference, version 1.8.6: https://www.ks.uiuc.edu/Research/vmd/vmd-1.8.6/ug/node124.html
- Compchems guide to VMD distance, angle, and dihedral measurements: https://www.compchems.com/vmd-measurements-analyze-distances-and-angles-with-vmd/#distance-measurements-in-vmd
