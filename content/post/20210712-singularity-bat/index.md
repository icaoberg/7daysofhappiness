---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "singularity-bat"
subtitle: "A cat(1) clone with syntax highlighting and Git integration."
summary: "A cat(1) clone with syntax highlighting and Git integration."
authors: ["icaoberg"]
tags: ["singularity", "github", "containerization", "utilities"]
categories: ["PSC"]
date: 2021-07-12T22:24:09
lastmod: 2021-07-12T22:24:09
featured: true
draft: false
image:

  caption: "GitHub repository"
  focal_point: "Smart"
  preview_only: true
---

![Example](https://camo.githubusercontent.com/7b7c397acc5b91b4c4cf7756015185fe3c5f700f70d256a212de51294a0cf673/68747470733a2f2f696d6775722e636f6d2f724773646e44652e706e67)

A cat(1) clone with syntax highlighting and Git integration.

* Singularity definition file [repository](https://github.com/pscedu/singularity-bat)
* Source code [repository](https://github.com/sharkdp/bat)

## To install this container on [Bridges 2](https://www.psc.edu/resources/bridges-2/)

Copy the

* `SIF` file
* and the `bat` script

to `/opt/packages/bat/0.17.1`.

Copy the file `modulefile.lua` to `/opt/modulefiles/bat` as `0.17.1.lua`.

## To load and use the module

```
> module load bat
> bat --help

bat 0.18.1
A cat(1) clone with syntax highlighting and Git integration.

USAGE:
    bat [OPTIONS] [FILE]...
    bat <SUBCOMMAND>

OPTIONS:
    -A, --show-all
            Show non-printable characters like space, tab or newline. This option can also be used
            to print binary files. Use '--tabs' to control the width of the tab-placeholders.
    -p, --plain
            Only show plain style, no decorations. This is an alias for '--style=plain'. When '-p'
            is used twice ('-pp'), it also disables automatic paging (alias for '--style=plain
            --pager=never').
    -l, --language <language>
            Explicitly set the language for syntax highlighting. The language can be specified as a
            name (like 'C++' or 'LaTeX') or possible file extension (like 'cpp', 'hpp' or 'md'). Use
            '--list-languages' to show all supported language names and file extensions.
    -H, --highlight-line <N:M>...
            Highlight the specified line ranges with a different background color For example:
              '--highlight-line 40' highlights line 40
              '--highlight-line 30:40' highlights lines 30 to 40
              '--highlight-line :40' highlights lines 1 to 40
              '--highlight-line 40:' highlights lines 40 to the end of the file
        --file-name <name>...
            Specify the name to display for a file. Useful when piping data to bat from STDIN when
            bat does not otherwise know the filename. Note that the provided file name is also used
            for syntax detection.
    -d, --diff
            Only show lines that have been added/removed/modified with respect to the Git index. Use
            --diff-context=N to control how much context you want to see.
        --diff-context <N>
            Include N lines of context around added/removed/modified lines when using '--diff'.

        --tabs <T>
            Set the tab width to T spaces. Use a width of 0 to pass tabs through directly

        --wrap <mode>
            Specify the text-wrapping mode (*auto*, never, character). The '--terminal-width' option
            can be used in addition to control the output width.
        --terminal-width <width>
            Explicitly set the width of the terminal instead of determining it automatically. If
            prefixed with '+' or '-', the value will be treated as an offset to the actual terminal
            width. See also: '--wrap'.
    -n, --number
            Only show line numbers, no other decorations. This is an alias for '--style=numbers'

        --color <when>
            Specify when to use colored output. The automatic mode only enables colors if an
            interactive terminal is detected - colors are automatically disabled if the output goes
            to a pipe.
            Possible values: *auto*, never, always.
        --italic-text <when>
            Specify when to use ANSI sequences for italic text in the output. Possible values:
            always, *never*.
        --decorations <when>
            Specify when to use the decorations that have been specified via '--style'. The
            automatic mode only enables decorations if an interactive terminal is detected. Possible
            values: *auto*, never, always.
    -f, --force-colorization
            Alias for '--decorations=always --color=always'. This is useful if the output of bat is
            piped to another program, but you want to keep the colorization/decorations.
        --paging <when>
            Specify when to use the pager. To disable the pager, use --paging=never' or its
            alias,'-P'. To disable the pager permanently, set BAT_PAGER to an empty string. To
            control which pager is used, see the '--pager' option. Possible values: *auto*, never,
            always.
        --pager <command>
            Determine which pager is used. This option will override the PAGER and BAT_PAGER
            environment variables. The default pager is 'less'. To control when the pager is used,
            see the '--paging' option. Example: '--pager "less -RF"'.
    -m, --map-syntax <glob:syntax>...
            Map a glob pattern to an existing syntax name. The glob pattern is matched on the full
            path and the filename. For example, to highlight *.build files with the Python syntax,
            use -m '*.build:Python'. To highlight files named '.myignore' with the Git Ignore
            syntax, use -m '.myignore:Git Ignore'. Note that the right-hand side is the *name* of
            the syntax, not a file extension.
        --theme <theme>
            Set the theme for syntax highlighting. Use '--list-themes' to see all available themes.
            To set a default theme, add the '--theme="..."' option to the configuration file or
            export the BAT_THEME environment variable (e.g.: export BAT_THEME="...").
        --list-themes
            Display a list of supported themes for syntax highlighting.

        --style <components>
            Configure which elements (line numbers, file headers, grid borders, Git modifications,
            ..) to display in addition to the file contents. The argument is a comma-separated list
            of components to display (e.g. 'numbers,changes,grid') or a pre-defined style ('full').
            To set a default style, add the '--style=".."' option to the configuration file or
            export the BAT_STYLE environment variable (e.g.: export BAT_STYLE="..").

            Possible values:

              * full: enables all available components.
              * auto: same as 'full', unless the output is piped (default).
              * plain: disables all available components.
              * changes: show Git modification markers.
              * header: show filenames before the content.
              * grid: vertical/horizontal lines to separate side bar
                      and the header from the content.
              * rule: horizontal lines to delimit files.
              * numbers: show line numbers in the side bar.
              * snip: draw separation lines between distinct line ranges.
    -r, --line-range <N:M>...
            Only print the specified range of lines for each file. For example:
              '--line-range 30:40' prints lines 30 to 40
              '--line-range :40' prints lines 1 to 40
              '--line-range 40:' prints lines 40 to the end of the file
              '--line-range 40' only prints line 40
    -L, --list-languages
            Display a list of supported languages for syntax highlighting.

    -u, --unbuffered
            This option exists for POSIX-compliance reasons ('u' is for 'unbuffered'). The output is
            always unbuffered - this option is simply ignored.
        --diagnostic
            Show diagnostic information for bug reports.

    -h, --help
            Print this help message.

    -V, --version
            Show version information.


ARGS:
    <FILE>...
            File(s) to print / concatenate. Use a dash ('-') or no argument at all to read from
            standard input.

SUBCOMMANDS:
    cache    Modify the syntax-definition and theme cache

Note: `bat -h` prints a short and concise overview while `bat --help` gives all details.
```
