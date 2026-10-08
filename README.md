# cfmleditor Scoop bucket

```powershell
scoop bucket add cfmleditor https://github.com/cfmleditor/scoop-bucket
scoop install cfmleditor/clif
```

| App | What it is |
|---|---|
| `clif` | The CFML language server and command-line checks, formerly cfmleditor-lsp. Installs `clif`, and `cfmleditor-lsp` beside it for editor extensions that still look for the old name. Windows on ARM runs the amd64 build. |

The manifest updates itself from [cfmleditor/clif](https://github.com/cfmleditor/clif)'s releases (`checkver`, `autoupdate`): a scheduled workflow (`excavator.yml`) checks for a new release, rewrites the version, URL and hash (read from the release's `checksums.txt`) and commits it. `test.yml` installs the manifest on Windows and runs it on every change.
