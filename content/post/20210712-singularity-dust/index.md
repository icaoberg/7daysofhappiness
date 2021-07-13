---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "singularity-dust"
subtitle: "du + rust = dust. Like du but more intuitive."
summary: "du + rust = dust. Like du but more intuitive."
authors: ["icaoberg"]
tags: ["singularity", "github", "containerization","utilities"]
categories: ["PSC"]
date: 2021-07-12T22:31:56
lastmod: 2021-07-12T22:31:56
featured: true
draft: false
image:

  caption: "GitHub repository"
  focal_point: "Smart"
  preview_only: true
---

![Example](https://raw.githubusercontent.com/bootandy/dust/master/media/snap.png)

du + rust = dust. Like du but more intuitive.

* Singularity definition file [repository](https://github.com/pscedu/singularity-dust)
* Source code [repository](https://github.com/bootandy/dust)

## To install this container on [Bridges 2](https://www.psc.edu/resources/bridges-2/)

Copy the

* `SIF` file
* and the `dust` script

to `/opt/packages/dust/0.5.4`.

Copy the file `modulefile.lua` to `/opt/modulefiles/dust` as `0.5.4.lua`.

## To load and use the module

```
> module load dust
> dust --help
Dust 0.6.0
Like du but more intuitive

USAGE:
    dust [FLAGS] [OPTIONS] [--] [inputs]...

FLAGS:
    -f, --filecount          Directory 'size' is number of child files/dirs not disk size
    -s, --apparent-size      Use file length instead of blocks
    -p, --full-paths         Subdirectories will not have their path shortened
    -h, --help               Prints help information
    -i, --ignore_hidden      Obey .git_ignore rules & Do not display hidden files
    -b, --no-percent-bars    No percent bars or percentages will be displayed
    -c, --no-colors          No colors will be printed (normally largest directories are colored)
    -r, --reverse            Print tree upside down (biggest highest)
    -V, --version            Prints version information

OPTIONS:
    -d, --depth <depth>                             Depth to show
    -X, --ignore-directory <ignore_directory>...    Exclude any file or directory with this name
    -n, --number-of-lines <number_of_lines>
            Number of lines of output to show. This is Height, (but h is help) [default: 20]

    -w, --terminal_width <width>
            Specify width of output overriding the auto detection of terminal width


ARGS:
    <inputs>...
```
