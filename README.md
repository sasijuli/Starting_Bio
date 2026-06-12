# Starting Bio

Starting Bio is a beginner-friendly collection of tutorials for learning tools commonly used in biomolecular modeling and molecular dynamics workflows.

The material is organized into three main modules:

- Linux command-line fundamentals
- VMD for molecular visualization and analysis
- NAMD for molecular dynamics simulations

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

## Module Contents

### 1. Linux Basics

- [Module overview](01-linux-basics/README.md)
- [Linux commands cheatsheet](01-linux-basics/commands-cheatsheet.md)
- [Practice exercises](01-linux-basics/exercises.md)

### 2. VMD

- [Module overview](02-vmd/README.md)
- [VMD Basics](02-vmd/vmd-basics/README.md)
- [VMD Pro](02-vmd/vmd-pro/README.md)

### 3. NAMD

- [Module overview](03-namd/README.md)
- [NAMD Basics](03-namd/namd-basics/README.md)
- [NAMD Pro](03-namd/namd-pro/README.md)

## Supporting Resources

- [Glossary](glossary.md): definitions of important Linux, VMD, and NAMD terms
- [External link summaries](link_summaries.md): short descriptions of selected supplementary resources
- [References](references.md): the complete list of external sources used in the tutorials
- [Tutorial page template](templates/tutorial-page-template.md): structure for adding a new tutorial page
- [Exercise template](templates/exercise-template.md): structure for adding a new exercise

When possible, this tutorial links to official documentation from Linux manual pages, VMD, and NAMD.

## Repository Structure

```text
Starting_bio/
├── 01-linux-basics/
│   ├── README.md
│   ├── commands-cheatsheet.md
│   └── exercises.md
├── 02-vmd/
│   ├── README.md
│   ├── vmd-basics/
│   │   ├── README.md
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
│       ├── advanced-tcl-and-automation.md
│       ├── trajectory-analysis.md
│       ├── protein-ligand-analysis.md
│       ├── membrane-analysis.md
│       ├── publication-graphics.md
│       └── large-systems-and-performance.md
├── 03-namd/
│   ├── README.md
│   ├── namd-basics/
│   │   ├── README.md
│   │   ├── installation.md
│   │   ├── input-files.md
│   │   ├── running-simulations.md
│   │   └── analyzing-results.md
│   └── namd-pro/
│       ├── README.md
│       ├── system-preparation-and-validation.md
│       ├── equilibration-and-production.md
│       ├── membrane-simulations.md
│       ├── free-energy-and-enhanced-sampling.md
│       ├── hpc-and-performance.md
│       ├── restarts-and-troubleshooting.md
│       └── reproducibility-and-data-management.md
├── templates/
│   ├── exercise-template.md
│   └── tutorial-page-template.md
├── README.md
├── glossary.md
├── link_summaries.md
└── references.md
```

## How To Use This Tutorial

1. Start with the module overview in each numbered folder.
2. Complete the `basics` section before moving to the corresponding `pro` section.
3. Read basic topic pages in the suggested order.
4. Choose advanced pages according to your scientific system or question.
5. Run the commands and complete the practice exercises.
6. Use the glossary when you encounter unfamiliar terminology.
7. Consult the external references for more detailed explanations.

The tutorial pages may include:

- Learning goals
- Core concepts
- Step-by-step notes
- Practice exercises
- External references
