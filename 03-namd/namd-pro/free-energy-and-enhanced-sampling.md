# How Can I Choose Enhanced-Sampling Or Free-Energy Methods?

## Scientific Question

How can I decide whether a standard trajectory is enough, or whether the scientific question needs steered MD, collective variables, umbrella sampling, ABF, replica exchange, metadynamics, FEP, or another enhanced method?

## Method Questions

### What coordinate describes the process?

Define the collective variable or reaction coordinate before choosing a method. If the coordinate is wrong, more sampling does not solve the interpretation problem.

### Am I exploring or estimating a free energy?

Use exploratory biased simulations to generate hypotheses or paths. Use umbrella sampling, ABF, FEP, or related methods when the goal is a quantitative free-energy estimate with uncertainty.

### How will I organize windows, replicas, or stages?

Record window centers, force constants, replica temperatures, lambda values, run lengths, restart files, random seeds, and analysis scripts. Keep every input and output tied to a manifest.

### How will I check convergence?

Compare independent repeats, forward and reverse paths, overlap between windows, uncertainty estimates, and sensitivity to analysis choices. Do not report a single curve without sampling evidence.

## Important Note

These methods require stronger statistical and physical justification than a standard simulation. Every future tutorial should state the method assumptions, sampling requirements, and uncertainty analysis explicitly.

## External References

- NAMD 3.0 User's Guide contents, accelerated sampling and QM/MM sections: https://www.ks.uiuc.edu/Research/namd/3.0/ug/node2.html
- NAMD bibliography for free-energy and rare-event methods: https://www.ks.uiuc.edu/Research/namd/2.14/ug/node120.html#MCCA87
- NAMD tutorial, steered molecular dynamics sections: https://www.ks.uiuc.edu/Training/Tutorials/namd/namd-tutorial-unix.pdf
- Scalable Molecular Dynamics with NAMD: https://pmc.ncbi.nlm.nih.gov/articles/PMC2486339/
