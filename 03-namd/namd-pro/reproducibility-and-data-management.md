# How Can I Make NAMD Simulations Reproducible?

## Scientific Question

How can I organize NAMD inputs, scripts, logs, restarts, trajectories, and analysis notes so another researcher can audit or repeat the workflow?

## Reproducibility Questions

### What must be recorded for every run?

Record NAMD version, build type, command line, job script, node/GPU configuration, config file, input coordinates, structure file, parameter files, restart files, random seeds, output prefixes, and analysis scripts.

### How should directories be organized?

Keep original inputs read-only. Use stage folders such as `00-build`, `01-minimize`, `02-heat`, `03-equilibrate`, `04-production`, and `analysis`. Put logs and restarts with the stage that produced them.

### How should Tcl scripting be handled?

NAMD configuration files can use Tcl features such as variables, `source`, environment variables, repeated `run` commands, callbacks, and scripted logic. These features are powerful, but they must be documented because they can hide important configuration choices.

### How should outputs be named?

Use stage-specific `outputname` and `restartname` prefixes. Never reuse the same prefix for separate stages unless the overwrite is intentional and documented.

## Suggested Outcome

Create a run manifest that records the inputs, configuration, software version, command, computing environment, outputs, and validation notes for every simulation stage.

## External References

- NAMD Tcl scripting interface and features: https://www.ks.uiuc.edu/Research/namd//2.5/ug/node11.html#section:tclscripting
- NAMD output and restart parameters: https://www.ks.uiuc.edu/Research/namd//2.5/ug/node14.html#param:outputname
- NAMD 2.14 release notes: https://www.ks.uiuc.edu/Research/namd/2.14/notes.html
- NAMD at TACC: https://docs.tacc.utexas.edu/software/namd/
- NAMD 3.0 User's Guide contents: https://www.ks.uiuc.edu/Research/namd/3.0/ug/node2.html
