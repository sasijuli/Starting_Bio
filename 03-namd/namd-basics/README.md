# NAMD Basics

## Learning Goals

By the end of this module, you should be able to:

- Explain what NAMD is used for
- Identify the basic input files needed for a simulation
- Understand the role of a NAMD configuration file
- Recognize common simulation output files

These skills are prerequisites for the specialized workflows in [NAMD Pro](../namd-pro/).

## Core Ideas

NAMD is a molecular dynamics simulation engine. It calculates how atoms move over time based on physical models called force fields.

## Common Input Files

- `.pdb`: Initial coordinates
- `.psf`: Molecular structure/topology information
- Parameter files: Force field parameters
- `.conf`: NAMD configuration file

## Common Output Files

- `.dcd`: Trajectory
- `.log`: Simulation log
- `.coor`: Coordinates
- `.vel`: Velocities
- `.xsc`: Extended system information

## Suggested Order

1. [Installation](installation.md)
2. [Input Files](input-files.md)
3. [Running Simulations](running-simulations.md)
4. [Analyzing Results](analyzing-results.md)

## External References

- NAMD documentation: https://www.ks.uiuc.edu/Research/namd/documentation.html
- Current NAMD User's Guide: https://www.tcbg.illinois.edu/Research/namd/current/ug.pdf
- NAMD tutorials: https://www.ks.uiuc.edu/Training/Tutorials/

## Next Step

After running and checking a small simulation, return to the [NAMD module overview](../README.md) or continue to [NAMD Pro](../namd-pro/).
