---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "singularity-visidata"
subtitle: "GitHub repository for the Singularity definition file"
summary: "GitHub repository for the Singularity definition file"
authors: ["icaoberg"]
tags: ["singularity", "github", "containerization", "utilities"]
categories: ["PSC"]
date: 2021-07-12T23:55:31
lastmod: 2021-07-12T23:55:31
featured: true
draft: false
image:

  caption: "GitHub repository"
  focal_point: "Smart"
  preview_only: true
---

VisiData is an interactive multitool for tabular data. It combines the clarity of a spreadsheet, the efficiency of the terminal, and the power of Python, into a lightweight utility which can handle millions of rows with ease.

* Singularity definition file [repository](https://github.com/pscedu/singularity-visidata)
* Source code [repository](https://www.visidata.org/)

## To install this container on [Bridges 2](https://www.psc.edu/resources/bridges-2/)

Copy the

* `SIF` file
* and the `vd` script

to `/opt/packages/visidata/2.4`.

Copy the file `modulefile.lua` to `/opt/modulefiles/visidata` as `2.4.lua`.

## To load and use the module

```
> module load visidata
> vd
```

## Example

[![asciicast](https://asciinema.org/a/SPyM2xkC7nXgDA7LPCSYizqkd.svg)](https://asciinema.org/a/SPyM2xkC7nXgDA7LPCSYizqkd)
