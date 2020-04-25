# temple README

This repository provides language support for Templefile.
For more information, see https://templeeight.github.io/temple-docs

## Direct Installation

To add this to your VSCode, run the following:

    ln -s "$(pwd)" ~/.vscode/extensions

To add it to IntelliJ, open Preferences › Editor › TextMate Bundles, and click add.

To build the JSON tmlanguage file, use the following command, using [`yaml2json`](https://www.npmjs.com/package/yaml2json):

    yaml2json syntaxes/temple.tmLanguage.yaml | python -m json.tool > syntaxes/temple.tmLanguage.json

This can be automated with [`entr`](http://eradman.com/entrproject/):

    entr -s "yaml2json syntaxes/temple.tmLanguage.yaml | python -m json.tool > syntaxes/temple.tmLanguage.json" <<< syntaxes/temple.tmLanguage.yaml


## Releases
### 0.0.1
Initial release of Templefile syntax

