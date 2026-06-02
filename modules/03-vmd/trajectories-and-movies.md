# Trajectories And Movies In VMD

## Goal

Learn how to load trajectory data, inspect motion over time, and create basic movies.

## What A Trajectory Is

A trajectory is a sequence of coordinate frames. In molecular dynamics, each frame represents the positions of atoms at a different time point.

Trajectory files, such as `.dcd` files, usually store coordinates but not complete structural information. For that reason, VMD often needs a structure file first, such as `.psf`, followed by the trajectory file.

## Loading A Trajectory

Basic workflow:

1. Open VMD.
2. Load the structure file first, for example a `.psf` file.
3. In the Molecule File Browser, keep the same molecule selected.
4. Load the trajectory file, for example a `.dcd` file.
5. Use the animation controls in the VMD Main window to move through frames.

When loading a trajectory, check whether you need to load every frame. Large trajectories can be slow, so frame stride can be useful.

## Visualizing Motion

Useful VMD trajectory tools include:

- Animation slider for moving through frames
- Loop, once, and rock playback modes
- Trajectory smoothing for reducing noisy visual motion
- Drawing multiple frames at once
- Updating atom selections every frame

The "update selection every frame" option is important for coordinate-dependent selections such as:

```text
water and within 3 of protein
```

Without updating, VMD may keep showing atoms that met the selection criteria in an earlier frame but no longer satisfy it later.

## Making Movies

VMD includes a Movie Maker plugin:

```text
Extensions > Visualization > Movie Maker
```

Beginner movie types include:

- A rotating movie of one frame
- A trajectory movie that advances through simulation frames
- A user-defined movie controlled by Tcl callbacks

For early practice, start with Snapshot rendering. More advanced rendering can use Tachyon or other renderers.

## Practice

1. Load a structure file and trajectory file.
2. Set the protein representation to `NewCartoon`.
3. Play the trajectory.
4. Try trajectory smoothing.
5. Draw every tenth frame from a section of the trajectory.
6. Create a short trajectory movie with Movie Maker.

## External References

- Official VMD tutorial, Trajectories and Movie Making: https://www.ks.uiuc.edu/Training/Tutorials/vmd/tutorial-html/node3.html
- VMD Images and Movies tutorial, Working With Trajectories: https://www.ks.uiuc.edu/Training/Tutorials/vmd-imgmv/imgmv/tutorial-html/node3.html
- VMD tutorials page: https://www.ks.uiuc.edu/Training/Tutorials/
- Current VMD User's Guide: https://www.ks.uiuc.edu/Research/vmd/current/ug.pdf
