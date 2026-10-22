# LocalGP Gridded Products

This org contains repos for producing gridded products with the LocalGP mapping algorithm. Usage generally proceeds as follows:

- **ocean_pipeline** is a preprocessing pipeline. It's responsibility is to consume upstream data in supported formats (ie, Argo data), perform data selection and filtration (by QC or otherwise), compute any derived quantities of interest (ie, potential temperature), package the result in files ready to be consumed by LocalGP, and set up LocalGP run directories populated with the selected data, code, and parameter files needed to launch the mapping algo.
- **LocalGP** is the mapping algorithm itself, combined with archiving tools for compressing and archiving key results.

Both repos come with slurm scripts for managing them on CU's blanca cluster; both repos contain more detailed documentation on config and use.

**Provenance records** are folded into the ocean_pipeline repo. These records indicate code and data versions and dependency stacks for labeled runs of LocalGP.
