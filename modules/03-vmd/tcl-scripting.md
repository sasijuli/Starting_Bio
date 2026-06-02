# Tcl Scripting In VMD

## Goal

Understand that VMD can be controlled with Tcl commands.

## Why This Matters

Scripts make analysis reproducible. Instead of manually clicking through the same steps, you can save commands and run them again.

VMD uses Tcl commands for many tasks that can also be done through the graphical interface. This is important because scripts can:

- Load molecules consistently
- Create selections
- Apply representations
- Extract coordinates or molecule information
- Repeat analysis over many frames

## Example

```tcl
mol new structure.pdb
mol representation NewCartoon
mol color Structure
mol addrep top
```

## Important Commands

### `atomselect`

The `atomselect` command creates an atom selection object. You can then ask that object for information such as atom names, indices, coordinates, residue names, or masses.

```tcl
set protein [atomselect top "protein"]
$protein num
$protein get name
$protein get {x y z}
$protein delete
```

Selections can also use a frame:

```tcl
set near_water [atomselect top "water and within 3 of protein" frame 10]
```

When writing longer scripts, delete selections when you are done with them. This keeps the script cleaner and avoids accumulating many temporary selections.

### `molinfo`

The `molinfo` command returns information about loaded molecules, such as the top molecule, number of atoms, number of frames, filename, file type, and current frame.

```tcl
molinfo list
molinfo top
molinfo top get numatoms
molinfo top get numframes
molinfo top get frame
```

This is especially useful when a script needs to know how many frames are available before looping through a trajectory.

## Practice

- Find the VMD Tk Console.
- Run a simple command.
- Save useful commands in a notes file.
- Create an atom selection for `protein`.
- Use `molinfo top get numframes` after loading a trajectory.

## External References

- VMD `atomselect` command reference: https://www.ks.uiuc.edu/Research/vmd/vmd-1.7.1/ug/node108.html
- VMD molecular analysis section, using `atomselect`: https://www.ks.uiuc.edu/Research/vmd/vmd-1.7.1/ug/node181.html
- VMD `molinfo` command reference: https://www.ks.uiuc.edu/Research/vmd/vmd-1.8.7/ug/node137.html
- Official VMD tutorial, Scripting in VMD: https://www.ks.uiuc.edu/Training/Tutorials/vmd/tutorial-html/index.html
