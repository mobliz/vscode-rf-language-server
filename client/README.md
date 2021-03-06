# Robot Framework Intellisense

A [Visual Studio Code](https://code.visualstudio.com/) extension that supports Robot Framework development.

## Features

### Syntax highlighting
* Supports `.robot` files
* Can be added for `.txt` files using the `files.associations` setting:
```json
"files.associations": {
    "*.txt": "robot"
}
```

### Goto definition
* For variables
* For user keywords
* `F12` on Mac, Linux and Windows

### Find all references
* For user keywords
* `⇧F12` on Mac, `Shift+F12` on Linux and Windows

### List file symbols
* Shows variables, keywords and test cases
* `⇧⌘O` on Mac, `Ctrl+Shift+O` on Linux and Windows

### List workspace symbols
* Shows variables, keywords and test cases
* `⌘T` on Mac, `Ctrl+T` on Linux and Windows

### Highlight All Occurrences of a Symbol in a Document
* Highlights all occurrences of a variable, keyword or setting
* Move the cursor to a variable, keyword or setting

### Show Code Completion Proposals
* Suggests user keywords and variables
* `⌃Space` on Mac, `Ctrl+Space` on Linux and Windows

### Support for python keywords
* Keywords defined in `.py` files are also included
* Requires that the `.py` files are included with `rfLanguageServer.includePaths` setting. E.g.
```json
"rfLanguageServer.includePaths": [
  "**/*.robot",
  "**/*.py"
]
```

## Configuration

By default all `.robot` files are parsed. This can be configured using parameters. (see `Code` > `Preferences` > `Workspace Settings`).

|param                            | description              |
|---------------------------------|--------------------------|
| `rfLanguageServer.includePaths` | Array of glob patterns for files to be included`|
| `rfLanguageServer.excludePaths` | Array of glob patterns for files to be excluded|
| `rfLanguageServer.logLevel` | What information of the language server is logged in the Output. Possible values `off`, `errors`, `info`, `debug`|
| `rfLanguageServer.trace.server` | what information of the communication between VSCode and the rfLanguageServer is logged to the Output. Possible values `off`, `messages`, `verbose`|

The `includePaths` and `excludePaths` properties take a list of glob-like file patterns. Even though any files can be matched this way, only files with supported extensions are included (i.e. `.robot`, `.txt`, and `.py`).

If the `includePaths` is left unspecified, the parser defaults to including all `.robot` files in the containing directory and subdirectories except those excluded using the `excludePaths` property.

## Known issues

Can be found [here](https://github.com/tomi/vscode-rf-language-server/blob/master/client/KNOWNISSUES.md)

## Changelog

Can be found [here](https://github.com/tomi/vscode-rf-language-server/blob/master/client/CHANGELOG.md).

## Bugs

Report them [here](https://github.com/tomi/vscode-rf-language-server/issues).


## License

[MIT](https://github.com/tomi/vscode-rf-language-server/blob/master/LICENSE)


## Acknowledgements

This project is a grateful recipient of the [Futurice Open Source sponsorship program](https://spiceprogram.org). ♥

Syntax highlighting grammar is built on top of [work](https://bitbucket.org/jussimalinen/robot.tmbundle/wiki/Home) by Jussi Malinen.
