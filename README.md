# Starting Bio

Starting Bio is a beginner-friendly collection of tutorials for learning tools commonly used in biomolecular modeling and molecular dynamics workflows.

The material is organized into five main modules:

- Linux command-line fundamentals
- VMD for molecular visualization and analysis
- NAMD for molecular dynamics simulations
- Batch computing for supercomputer job scheduling
- Useful tools for membrane analysis

## Who This Is For

This guide is designed for students or new researchers who want to understand how Linux, VMD, and NAMD work together in a practical scientific workflow.

No advanced programming background is assumed, but basic comfort with computers is helpful.

## Tutorial Roadmap

Work through the modules in numerical order:

1. [Linux Basics](01-linux-basics/)
   Learn command-line navigation, file management, documentation, and essential Linux commands.
2. [VMD](02-vmd/)
   Start with core visualization and analysis, then continue to advanced or system-specific workflows.
3. [NAMD](03-namd/)
   Start with simulation inputs and execution, then continue to advanced simulation design and specialized methods.
4. [Batch Computing](04-batch-computing/)
   Learn the basics of Slurm batch jobs before running demanding workloads on a supercomputer.
5. [Useful Tools For Membrane Analysis](05-useful-tools-for-membrane-analysis/)
   Collect external GitHub tools for membrane simulation analysis.

## Module Contents

### 1. Linux Basics

- [Module overview](01-linux-basics/README.md)
- [Linux commands cheatsheet](01-linux-basics/commands-cheatsheet.md)
- [Practice exercises](01-linux-basics/exercises.md)
- [Linux references](01-linux-basics/references.md)

### 2. VMD

- [Module overview](02-vmd/README.md)
- [VMD Basics](02-vmd/vmd-basics/README.md)
- [VMD Pro](02-vmd/vmd-pro/README.md)
- [VMD references](02-vmd/references.md)
- [VMD supplementary link summaries](02-vmd/link_summaries.md)

### 3. NAMD

- [Module overview](03-namd/README.md)
- [NAMD Basics](03-namd/namd-basics/README.md)
- [NAMD Pro](03-namd/namd-pro/README.md)
- [NAMD references](03-namd/references.md)

### 4. Batch Computing

- [Module overview](04-batch-computing/README.md)
- External Slurm tutorial: https://github.com/mkandes/batch-computing/blob/main/BATCH.md

### 5. Useful Tools For Membrane Analysis

- [Module overview](05-useful-tools-for-membrane-analysis/README.md)
- MembraneAnalysis.jl: https://github.com/amiralih/MembraneAnalysis.jl
- qwrap, fast PBC wrapping and unwrapping for VMD: https://github.com/jhenin/qwrap

## Supporting Resources

- [Glossary](glossary.md): definitions of important Linux, VMD, and NAMD terms
- [VMD supplementary link summaries](02-vmd/link_summaries.md): optional VMD articles, videos, tutorials, and notes organized by topic
- [References](references.md): the complete list of external sources used in the tutorials
- [Tutorial page template](templates/tutorial-page-template.md): structure for adding a new tutorial page
- [Exercise template](templates/exercise-template.md): structure for adding a new exercise

## Reference Index

Use the main [reference list](references.md) when you need sources grouped by topic.

- Linux: command-line manuals and documentation sources
- VMD basics: installation, visualization, atom selections, Tcl commands, measurements, trajectories, and movies
- VMD advanced: automation, trajectory analysis, protein-ligand analysis, membrane workflows, publication graphics, and large-system performance
- NAMD basics: installation, input files, running simulations, and analyzing outputs
- NAMD advanced: system preparation, equilibration, membranes, enhanced sampling, HPC, restarts, troubleshooting, and reproducibility
- Batch computing: Slurm job scheduling, login-node rules, queues, nodes, job arrays, and dependencies
- Membrane analysis tools: GitHub repositories for lipid membrane and membrane-protein analysis workflows

When possible, this tutorial links to official documentation from Linux manual pages, VMD, and NAMD.

## How To Use This Tutorial

1. Start with the module overview in each numbered folder.
2. Complete the `basics` section before moving to the corresponding `pro` section.
3. Read basic topic pages in the suggested order.
4. Choose advanced pages according to your scientific system or question.
5. Complete the batch-computing module before running long jobs on a supercomputer.
6. Run the commands and complete the practice exercises.
7. Use the glossary when you encounter unfamiliar terminology.
8. Consult the external references for more detailed explanations.

The tutorial pages may include:

- Learning goals
- Core concepts
- Step-by-step notes
- Practice exercises
- External references

## Repository Structure

```text
Starting_bio/
├── 01-linux-basics/
│   ├── README.md
│   ├── commands-cheatsheet.md
│   ├── exercises.md
│   └── references.md
├── 02-vmd/
│   ├── README.md
│   ├── references.md
│   ├── link_summaries.md
│   ├── vmd-basics/
│   │   ├── README.md
│   │   ├── references.md
│   │   ├── installation.md
│   │   ├── visualization.md
│   │   ├── atom-selections.md
│   │   ├── tcl-scripting.md
│   │   ├── measurements.md
│   │   ├── analysis.md
│   │   ├── trajectories-and-movies.md
│   │   └── tutorial-resources.md
│   └── vmd-pro/
│       ├── README.md
│       ├── references.md
│       ├── advanced-tcl-and-automation.md
│       ├── trajectory-analysis.md
│       ├── protein-ligand-analysis.md
│       ├── membrane-analysis.md
│       ├── publication-graphics.md
│       └── large-systems-and-performance.md
├── 03-namd/
│   ├── README.md
│   ├── references.md
│   ├── namd-basics/
│   │   ├── README.md
│   │   ├── references.md
│   │   ├── installation.md
│   │   ├── input-files.md
│   │   ├── running-simulations.md
│   │   └── analyzing-results.md
│   └── namd-pro/
│       ├── README.md
│       ├── references.md
│       ├── system-preparation-and-validation.md
│       ├── equilibration-and-production.md
│       ├── membrane-simulations.md
│       ├── free-energy-and-enhanced-sampling.md
│       ├── hpc-and-performance.md
│       ├── restarts-and-troubleshooting.md
│       └── reproducibility-and-data-management.md
├── 04-batch-computing/
│   └── README.md
├── 05-useful-tools-for-membrane-analysis/
│   └── README.md
├── templates/
│   ├── exercise-template.md
│   └── tutorial-page-template.md
├── README.md
├── glossary.md
└── references.md
```
