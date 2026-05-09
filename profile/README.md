# allay

A package manager for [CC: Tweaked](https://tweaked.cc).

Install:

```
wget run https://raw.githubusercontent.com/allaycc/allay/main/install.lua
```

## Repos

| Repo | What it is |
|---|---|
| [allay](https://github.com/allaycc/allay) | The CLI and runtime. `allay install`, `allay update`, etc. |
| [core](https://github.com/allaycc/core) | The default package source. Hosts allay itself plus its foundation libs. |
| [extras](https://github.com/allaycc/extras) | Curated catalog of popular CC: Tweaked libraries (Pine3D, ecnet2, msks, ...). |
| [lualibs](https://github.com/allaycc/lualibs) | Foundation libraries: hash, pathkit, log, httpkit, argparse, levenshtein, ui, scout. Reusable outside allay. |
| [unicornpkg-compat](https://github.com/allaycc/unicornpkg-compat) | Translator for installing unicornpkg-format packages through allay. |
| [spec](https://github.com/allaycc/spec) | Versioned format specs: package definition, source index, lockfile. |
| [server](https://github.com/allaycc/server) | Serve allay packages over rednet (experimental). |
| [rednet-transport](https://github.com/allaycc/rednet-transport) | rednet:// transport plugin so clients can fetch packages from an allay-server (experimental). |
