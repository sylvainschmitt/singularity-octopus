[Octopus](https://github.com/luntergroup/octopus)
[Singularity](https://github.com/hpcng/singularity) container
================
Sylvain Schmitt
April 28, 2021

**Bionformatics software Octopus**

Octopus is a mapping-based variant caller that implements several
calling models within a unified haplotype-aware framework. Octopus takes
inspiration from particle filtering by constructing a tree of haplotypes
and dynamically pruning and extending the tree based on haplotype
posterior probabilities in a sequential manner. This allows octopus to
implicitly consider all possible haplotypes at a given loci in
reasonable time.

Octopus Version: 0.7.4

\[<https://github.com/luntergroup/octopus>\]

Singularity container based on the recipe: Singularity.template.def

Package installation using Miniconda3 V4.7.12

Image singularity (V\>=3.3) is automatically test and built and pushed
on the registry using
[test.yml](https://github.com/sylvainschmitt/singularity-template/blob/main/.github/workflows/test.yml)
&
[builder.yml](https://github.com/sylvainschmitt/singularity-template/blob/main/.github/workflows/builder.yml)

**build**:

``` bash
sudo singularity build octopus.sif Singularity
singularity run octopus.sif
singularity exec octopus.sif octopus -h
```

**pull**:

``` bash
singularity pull https://github.com/sylvainschmitt/singularity-octopus/releases/download/0.0.1/sylvainschmitt-singularity-octopus.latest.sif
```

**snakemake**:

``` python
    singularity: 
        "https://github.com/sylvainschmitt/singularity-octopus/releases/download/0.0.1/sylvainschmitt-singularity-octopus.latest.sif"
```
