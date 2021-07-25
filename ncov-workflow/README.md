# About

This repository analyzes viral genomes using [Nextstrain](https://nextstrain.org) to understand how SARS-CoV-2, the virus that is responsible for the COVID-19 pandemic, evolves and spreads. This workflow is copied from [github.com/nextstrain/ncov](https://github.com/nextstrain/ncov).

# Running

After installing Nextstrain dependencies this workflow can be run as:
```
snakemake -j 1 -p --profile adaptive_evolution_profiles/adaptive-evolution
```

However, running via cluster or AWS will be faster:
```
nextstrain build --aws-batch --cpus 96 --memory 180GiB --detach . --set-threads tree=16
```