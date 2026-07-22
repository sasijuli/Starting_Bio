# Analysis In VMD

## Goal

Introduce basic analysis tasks in VMD.

## Examples

- Measuring distances
- Selecting atoms
- Viewing trajectories
- Tracking structural changes over time
- Calculating RMSD, RMSF, contacts, radius of gyration, or hydrogen bonds with Tcl commands

## Analysis Workflow

Begin with visual inspection, then move toward reproducible measurements.

1. Load the structure and, if available, the trajectory.
2. Choose the atom selection that matches the question.
3. Decide whether the analysis should use one frame or many frames.
4. Use the GUI for quick checks.
5. Use Tcl commands for repeatable analysis.
6. Save results in a text file when the data should be plotted or reused.

For quick interactive measurements, use labels and the mouse pick modes. For scripted analysis, use `atomselect` together with commands such as `measure center`, `measure bond`, `measure angle`, `measure dihed`, `measure rmsd`, or `measure rgyr`.

## Practice

Use VMD to measure the distance between two atoms in a structure.

Record:

- The atom names
- The residue names
- The measured distance

Then repeat the same idea with an angle and a dihedral. If you have a trajectory loaded, record whether the value changes as the frames advance.

## External References

- VMD `measure` command reference, version 1.8.5: https://www.ks.uiuc.edu/Research/vmd/vmd-1.8.5/ug/node124.html
- VMD `measure` command reference, version 1.8.6: https://www.ks.uiuc.edu/Research/vmd/vmd-1.8.6/ug/node124.html
- Compchems guide to VMD distance, angle, and dihedral measurements: https://www.compchems.com/vmd-measurements-analyze-distances-and-angles-with-vmd/#tracking-distance-during-the-simulation
