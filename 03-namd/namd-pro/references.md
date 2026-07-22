# NAMD Pro References

These references support advanced system preparation, equilibration, production simulations, membrane systems, enhanced sampling, HPC execution, restarts, and reproducibility.

## Core Official Documentation

- Current NAMD User's Guide: https://www.ks.uiuc.edu/Research/namd/current/ug.pdf
- NAMD documentation archive: https://www.ks.uiuc.edu/Research/namd/documentation.html
- NAMD tutorials page: https://www.ks.uiuc.edu/Training/Tutorials/
- NAMD mailing list: https://www.ks.uiuc.edu/Research/namd/mailing_list/

## System Preparation And Membranes

- VMD plugins for Psfgen, AutoPSF, Solvate, AutoIonize, Membrane, and QwikMD: https://www.ks.uiuc.edu/Research/vmd/plugins/
- CHARMM-GUI: https://www.charmm-gui.org/
- Introductory Membrane Proteins tutorial listing: https://www.ks.uiuc.edu/Training/Tutorials/
- Advanced Membrane Proteins tutorial: https://www.ks.uiuc.edu/Training/Tutorials/tutorialfiles/memb.prot.advanced/TCBGTUTORIAL_MEMBRANE_PROTEINS_I.pdf
- NAMD tutorial, Unix/MacOSX PDF: https://www.ks.uiuc.edu/Training/Tutorials/namd/namd-tutorial-unix.pdf
- NAMD tutorial, PSF files: https://www.ks.uiuc.edu/Training/Tutorials/namd/namd-tutorial-unix-html/node23.html
- NAMD tutorial, parameter files: https://www.ks.uiuc.edu/Training/Tutorials/namd/namd-tutorial-unix-html/node25.html#:~:text=given%20in%20the%20parameter%20files,/mole/rad**2%20!
- NAMD constraints and restraints: https://www.ks.uiuc.edu/Research/namd/2.13/ug/node27.html
- CHARMM force field files, MacKerell Lab: https://mackerell.umaryland.edu/charmm_ff.shtml
- NAMD-L TIP4P discussion: https://www.ks.uiuc.edu/Research/namd/mailing_list/namd-l.2010-2011/2303.html
- Scalable Molecular Dynamics with NAMD: https://pmc.ncbi.nlm.nih.gov/articles/PMC2486339/

## Equilibration, Production, And Controls

- NAMD configuration parameters, timestep and basic dynamics: https://www.ks.uiuc.edu/Research/namd/2.6/olddocs/ug/node26.html
- NAMD standard minimization and dynamics parameters: https://www.ks.uiuc.edu/Research/namd/2.14/ug/node34.html
- NAMD temperature control and equilibration: https://www.ks.uiuc.edu/Research/namd/2.14/ug/node38.html#SECTION000104100000000000000
- NAMD pressure control: https://www.ks.uiuc.edu/Research/namd/3.0b3/ug/node39.html

## Free Energy And Enhanced Sampling

- NAMD User's Guide sections on collective variables and alchemical free-energy calculations: https://www.ks.uiuc.edu/Research/namd/current/ug.pdf
- Colvars documentation: https://colvars.github.io/
- NAMD free-energy and enhanced-sampling tutorials: https://www.ks.uiuc.edu/Training/Tutorials/
- Metadynamics tutorial: https://www.ks.uiuc.edu/Training/Tutorials/namd/metadynamics-tutorial/meta-tutorial.pdf
- Streamlined Alchemical Free Energy Perturbation tutorial: https://livecomsjournal.org/index.php/livecoms/article/view/v5i1e2067
- NAMD 2.14 bibliography and method references: https://www.ks.uiuc.edu/Research/namd/2.14/ug/node120.html#MCCA87
- NAMD 3.0 User's Guide contents for accelerated sampling, constant pH, QM/MM, and runtime analysis: https://www.ks.uiuc.edu/Research/namd/3.0/ug/node2.html

## HPC, Performance, And Restarts

- NAMD User's Guide sections on running NAMD, performance, GPU execution, output, and restart files: https://www.ks.uiuc.edu/Research/namd/current/ug.pdf
- NAMD at TACC: https://docs.tacc.utexas.edu/software/namd/
- NAMD at Texas wiki page: https://www.ks.uiuc.edu/Research/namd/wiki/index.cgi?NamdAtTexas
- NAMD performance tuning concepts: https://www.ks.uiuc.edu/Research/namd/2.13/ug/node91.html
- NAMD output and restart parameters: https://www.ks.uiuc.edu/Research/namd//2.5/ug/node14.html#param:outputname
- NAMD Tcl scripting in configuration files: https://www.ks.uiuc.edu/Research/namd//2.5/ug/node11.html#section:tclscripting
- NAMD-L XST format discussion: https://www.ks.uiuc.edu/Research/namd/mailing_list/namd-l.2003-2004/0234.html
- NAMD 2.14 release notes and problem-reporting guidance: https://www.ks.uiuc.edu/Research/namd/2.14/notes.html
- Getting Started with Batch Job Scheduling: Slurm Edition: https://github.com/mkandes/batch-computing/blob/main/BATCH.md

Cluster-specific scheduler syntax and resource policies should come from the documentation maintained by the institution that operates the cluster.

## Video Tutorials

### Introductory NAMD And VMD Workflow

- Introduction to VMD and NAMD - Emad Tajkhorshid: https://www.youtube.com/watch?v=VdfeUSB3VZA

### Running NAMD Simulations

- Intro to Running Molecular Dynamics Simulations with NAMD: https://www.youtube.com/watch?v=xS4r2bLATvo&t=638s

## Suggested Sources By Page

- `system-preparation-and-validation.md`: NAMD User's Guide, NAMD tutorial PSF and parameter file sections, VMD plugins, MacKerell force fields, TIP4P discussion, and CHARMM-GUI
- `equilibration-and-production.md`: NAMD User's Guide, standard minimization and dynamics parameters, thermostat controls, pressure controls, and official NAMD tutorial
- `membrane-simulations.md`: membrane tutorials, CHARMM-GUI, pressure control, restraints, useful membrane-analysis tools, and the NAMD User's Guide
- `free-energy-and-enhanced-sampling.md`: NAMD User's Guide, Colvars, enhanced-sampling tutorials, NAMD bibliography, and NAMD 3.0 method sections
- `hpc-and-performance.md`: NAMD User's Guide, NAMD at TACC, NAMD at Texas, performance tuning, and the batch-computing module
- `restarts-and-troubleshooting.md`: NAMD User's Guide, output and restart parameters, XST discussion, release notes, temperature controls, pressure controls, and mailing list
- `reproducibility-and-data-management.md`: NAMD Tcl scripting, output naming, User's Guide, software versions, and cluster records for each run

## Related Repository Resources

- [NAMD Pro overview](README.md)
- [NAMD module references](../references.md)
- [VMD Pro](../../02-vmd/vmd-pro/)
- [Complete repository references](../../references.md)
