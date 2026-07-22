# How Can I Run NAMD Efficiently On A Supercomputer?

## Scientific Question

How can I choose resources, run benchmarks, and submit NAMD jobs without wasting allocation time or violating cluster policy?

## Performance Questions

### What should I benchmark?

Benchmark the exact system, force-field settings, cutoff, PME settings, CPU/GPU build, and node type intended for production. Startup overhead can distort short tests, so use normal dynamics and read NAMD `Benchmark time:` and `TIMING:` lines after startup and load balancing.

### How many nodes should I request?

More nodes are not always faster per allocation unit. Test a few resource configurations and compare ns/day, queue wait, allocation charge, and scaling efficiency.

### How should I submit jobs?

Use local cluster documentation for scheduler syntax. At TACC, the NAMD page provides system-specific examples, modules, and sample job scripts. The exact commands will differ on other clusters.

### What output costs matter?

Trajectory, restart, and log frequency affect filesystem load and storage use. Match output frequency to analysis needs and wall-time risk.

## Suggested Outcome

Create a benchmark table for several CPU/GPU and node-count configurations before selecting settings for a long simulation.

## Batch Computing Prerequisite

Before submitting NAMD jobs to a supercomputer, complete the [Batch Computing On Supercomputers](../../04-batch-computing/) module.

## External References

- Getting Started with Batch Job Scheduling: Slurm Edition: https://github.com/mkandes/batch-computing/blob/main/BATCH.md
- NAMD at TACC: https://docs.tacc.utexas.edu/software/namd/
- NAMD performance tuning concepts: https://www.ks.uiuc.edu/Research/namd/2.13/ug/node91.html
- NAMD 3.0 User's Guide contents, running NAMD and GPU acceleration sections: https://www.ks.uiuc.edu/Research/namd/3.0/ug/node2.html
- NAMD at Texas wiki page: https://www.ks.uiuc.edu/Research/namd/wiki/index.cgi?NamdAtTexas
- NAMD 2.14 release notes: https://www.ks.uiuc.edu/Research/namd/2.14/notes.html
