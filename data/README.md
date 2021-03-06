# Data files for intellisense

We describe how the data files used for intellisense are generated.

## Unicode mathematical symbols

The file `unimathsymbols.json` is generated from the [`unimathsymbols.txt`](http://milde.users.sourceforge.net/LUCR/Math/data/unimathsymbols.txt) by Günter Milde using the [`unimathsymbols.py`](../dev/unimathsymbols.py) script.

## Default commands and environments

Default lists of commands and environments are defined in

- [`commands.json`](commands.json)
- [`environments.json`](environments.json)

## Bibtex

The file [`bibtex-entries.json`](]bibtex-entries.json) lists for every bibtex entry type the mandatory fields. The file [`bibtex-optional-entries.json`](]bibtex-optional-entries.json) lists for every bibtex entry type the optional fields.

## Files inside `packages/`

JSON files in this directory and in the subdirectories are generated from the [cwl files by the LaTeXing project](https://github.com/LaTeXing/LaTeX-cwl) by the [`pkgcommand.py`](../dev/pkgcommand.py) script.

For every package/class, two files are generated

- a `_cmd.json` file listing all the commands defined by the package/class;
- a `_env.json` file listing all the environments defined by the package/class in the form.

Completion files for classes are all prefixed by `class-`.

See [dev/README.md](../dev/README.md#pkgcommand.py) for the description of the file formats.

## Class names

Class names are stored in [`classnames.json`](classnames.json)

This file is generated by the [`ctanpkglist.py`](../dev/ctanpkglist.py) script.

**Note that this file depends on the local LaTeX installation.**

## Class and package names

Package names are stored in [`packagenames.json`](packagenames.json)

This file is based on the list provided by [CTAN](https://ctan.org/json/2.0/packages) and on the [`ctanpkglist.py`](../dev/ctanpkglist.py) script.

See [dev/README.md](../dev/README.md#ctanpkglist.py) for the description of how this file is computed.

## Misc

We have to use four backslashes `\\\\` in some snippet definitions. See  the [official document](https://code.visualstudio.com/docs/editor/userdefinedsnippets#_grammar), [microsoft/vscode/issues/32020](https://github.com/microsoft/vscode/issues/32020), and [microsoft/vscode/issues/33933](https://github.com/microsoft/vscode/issues/33933) for the details.
