---
title: "`pixi` and `uv`"
date: "2025-03-26"
author:
  - name: "Matt Fisher"
    orcid: "0000-0003-3260-5445"
image: "pixi.png"
---

`pixi` and `uv` are part of a new generation of environment management tools that are
fast, ergonomic, and featureful.

::: {.callout-note}
This is a note! [Callout docs](https://quarto.org/docs/authoring/callouts.html)
:::

## Fast

`pixi` and `uv` are written in Rust as alternatives to slower Python-based tools `conda`
and `pip`.


## Ergonomic

`pixi` and `uv` implement commands and behaviors which replace frequently-manual work
like initializing a project, installing dependencies, maintaining an environment spec
file, and generating a lock file.


## Featureful

`pixi` and `uv` include features that are often cobbled together from multiple tools
under one roof.

`uv` supports creating a new environment (`venv`), installing dependencies (`pip`),
managing a lockfile (`pipenv`), running tasks (`invoke`, `nox`, `tox`), and more.

`pixi` similarly supports creating new environments and installing dependencies
(`conda`, `mamba`, `micromamba`), managing a lockfile (`conda-lock`), running tasks
(same as above), and more.

## Conclusion

Installing `uv` or `pixi` is quick and easy.

To [install uv](https://docs.astral.sh/uv/getting-started/installation/):

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

To [install pixi](https://pixi.sh/dev/#installation):

```bash
curl -fsSL https://pixi.sh/install.sh | bash
```
