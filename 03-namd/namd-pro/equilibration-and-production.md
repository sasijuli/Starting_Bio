# How Can I Equilibrate A System Before Production?

## Scientific Question

How can I move from minimization to stable production dynamics without shocking the system or hiding unstable behavior?

## Staged Workflow

1. Minimize bad contacts with restrained heavy atoms if needed.
2. Heat gradually to the target temperature.
3. Equilibrate at constant volume or constant pressure according to system needs.
4. Release positional restraints in stages.
5. Start production only after energy, temperature, pressure, volume, and key structural metrics are stable enough for the scientific question.

## Equilibration Questions

### Which thermostat should I use?

NAMD supports Langevin dynamics, temperature coupling, stochastic velocity rescaling, temperature rescaling, and reassignment. Choose one method intentionally and record the target temperature, damping or coupling settings, and whether coupling applies to hydrogens.

### When should I use pressure control?

Use pressure control for periodic systems where volume and density should relax. Constant pressure requires periodic boundary conditions. For biomolecular systems, expect large instantaneous pressure fluctuations; interpret averaged pressure and volume trends instead of single-frame values.

### How often should I write output?

Write logs often enough to detect instability, but not so often that I/O dominates the run. Keep restart output frequent enough for the queue wall time and storage policy.

### When is a system ready for production?

Look for stable temperature, reasonable energy drift, relaxed volume or area, no exploding forces, no persistent bad contacts, and structural metrics that are consistent with the intended ensemble.

## Suggested Output

Separate configuration files for minimization, heating, restrained equilibration, restraint-release stages, and production. Each file should specify the previous stage it depends on and the restart files it uses.

## External References

- NAMD standard minimization and dynamics parameters: https://www.ks.uiuc.edu/Research/namd/2.14/ug/node34.html
- NAMD temperature control and equilibration: https://www.ks.uiuc.edu/Research/namd/2.14/ug/node38.html#SECTION000104100000000000000
- NAMD pressure control: https://www.ks.uiuc.edu/Research/namd/3.0b3/ug/node39.html
- NAMD configuration parameters, timestep and basic dynamics: https://www.ks.uiuc.edu/Research/namd/2.6/olddocs/ug/node26.html
- NAMD tutorial, Unix/MacOSX PDF: https://www.ks.uiuc.edu/Training/Tutorials/namd/namd-tutorial-unix.pdf
