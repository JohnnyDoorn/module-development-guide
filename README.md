# JASP Module Development Guide

This guide covers everything you need to know to develop a JASP module — from setting up your environment to publishing in the JASP Module Library.

**Read the guide online:** https://johnnydoorn.github.io/module-development-guide/

## What is a JASP module?

A JASP module is an extension that adds new statistical analyses to JASP. Internally, a JASP module is an R package with additional QML files for the graphical interface:

- **R code** — your statistical computations, using any CRAN/Bioconductor packages
- **QML interface** — the options panel users interact with
- **jaspResults** — the bridge that renders tables, plots, and text in JASP's output

## How the guide is organised

**Building Your Module** walks you through the core development process. You'll learn how a module is structured, how to design the user-facing options panel in QML, how to write the R analysis backend using the jaspResults API, how QML and R are connected, and how to use jaspTools during development.

**Improving Your Module** covers everything that makes your module robust and maintainable. This includes coding standards, writing helpful error messages, testing your analyses, debugging when things go wrong, translating your module for international users, and handling backward compatibility when upgrading your QML interface.

**Finalizing Your Module** guides you through the steps to share your work with the world. You'll learn about versioning, publishing to the JASP Module Library, the Git workflow for contributing to JASP, licensing, building JASP from source (for core developers), and using AI tools to assist your development.

## Quick start

1. Fork [jaspModuleTemplate](https://github.com/jasp-stats/jaspModuleTemplate)
2. Clone it locally
3. Install [JASP nightly](http://static.jasp-stats.org/Nightlies/)
4. Install your module as a development module in JASP
5. Edit R and QML files, recompile, refresh — iterate

## Building the guide locally

This guide is built with [Quarto](https://quarto.org/). To render it locally:

```bash
quarto render
```

The output is generated in the `docs/` folder.
