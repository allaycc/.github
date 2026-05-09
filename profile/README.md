# allay

the only cc package manager that actually manages packages. for [cc: tweaked](https://tweaked.cc).

## install

```
wget run https://raw.githubusercontent.com/allaycc/allay/main/install.lua
```

# why allay

most cc software gets installed with `wget run`, which is fine, until you're installing programs that depend on other programs that depend on libraries that depend on other libraries.

allay handles the actual problem. dependencies install themselves, updates apply across everything at once, and removals can clean up the things that came along just for the package you're removing.

# "but i already use unicornpkg"

your packages install through allay the same as any other. when a unicornpkg-format package shows up, allay translates it on read. same install command, same lockfile, same dep resolution. you don't have to migrate. you don't have to choose between catalogs.

# "can i install a library that isn't built for allay specifically"

yes. give allay a github repo and it walks the tree itself: figures out which files are libraries, which are programs, where each one goes, and what other packages it needs. you don't need the author to publish anything. for allay, the source code is the package.

## Repos

| repo | what to find |
|---|---|
| [allay](https://github.com/allaycc/allay) | The CLI and runtime. `allay install`, `allay update`, etc. |
| [core](https://github.com/allaycc/core) | The default package source. Hosts allay itself plus its foundation libs. |
| [extras](https://github.com/allaycc/extras) | Curated catalog of popular CC: Tweaked libraries (Pine3D, ecnet2, msks, ...). |
| [lualibs](https://github.com/allaycc/lualibs) | Foundation libraries: hash, pathkit, log, httpkit, argparse, levenshtein, ui, scout. Reusable outside allay. |
| [alicorn](https://github.com/allaycc/alicorn) | Translator for installing unicornpkg-format packages through allay. |
| [spec](https://github.com/allaycc/spec) | Versioned format specs: package definition, source index, lockfile. |
| [server](https://github.com/allaycc/server) | Serve allay packages over rednet (experimental). |
| [rednet-transport](https://github.com/allaycc/rednet-transport) | rednet:// transport plugin so clients can fetch packages from an allay-server (experimental). |
