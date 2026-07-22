# How Can I Restart And Troubleshoot NAMD Simulations?

## Scientific Question

How can I continue an interrupted simulation and diagnose failures without mixing incompatible restart files or hiding the original problem?

## Restart Questions

### Which files define the restart state?

Use coordinate, velocity, and extended-system restart files from the same saved step. For constant-pressure simulations, the extended-system file records periodic cell information and should not be omitted.

### How should output names be handled?

Use `outputname`, `restartname`, and `firsttimestep` intentionally so that new outputs do not overwrite previous stages. The older NAMD documentation remains useful for understanding how output and restart prefixes map to files.

### How do I interpret XST files?

An XST file records timestep, unit cell vectors, cell origin, and extended system variables. Use it when reconstructing periodic cell history or diagnosing pressure/box behavior.

### What should I preserve after a failure?

Keep the config file, log, recent restart files, parameter files, job script, module list, NAMD version, and exact command. Do not delete failed inputs until the cause is known.

## Troubleshooting Checklist

- Confirm all restart files come from the same step.
- Check the first fatal error, not only the final scheduler message.
- Inspect temperature, pressure, volume, total energy, and bad contacts.
- Verify parameter files and atom names when errors mention missing parameters.
- Re-run a short test from the restart before submitting a long continuation.

## External References

- NAMD output and restart parameters: https://www.ks.uiuc.edu/Research/namd//2.5/ug/node14.html#param:outputname
- NAMD-L XST format discussion: https://www.ks.uiuc.edu/Research/namd/mailing_list/namd-l.2003-2004/0234.html
- NAMD 2.14 release notes, problem-reporting guidance: https://www.ks.uiuc.edu/Research/namd/2.14/notes.html
- NAMD temperature control and equilibration: https://www.ks.uiuc.edu/Research/namd/2.14/ug/node38.html#SECTION000104100000000000000
- NAMD pressure control: https://www.ks.uiuc.edu/Research/namd/3.0b3/ug/node39.html
