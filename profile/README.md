# allay

the package manager you should use for your craft-os // [cc: tweaked](https://tweaked.cc).

# why allay

most cc software gets installed with `wget run`, which is fine, until you're installing programs that depend on other programs that depend on libraries that depend on other libraries.

allay handles the actual problem. dependencies install themselves, updates apply across everything at once, and removals can clean up the things that came along just for the package you're removing.

# "but i already use unicornpkg"

we support unicornpkg packages, and even more.

# "can i install a library that isn't built for allay specifically"

yes you can. allay handles it. you'd be surprised.

Install:

```
wget run https://raw.githubusercontent.com/allaycc/allay/main/install.lua
```

## Repos

| repo | what to find |
|---|---|
| [allay](https://github.com/allaycc/allay) | The CLI and runtime. `allay install`, `allay update`, etc. |
| [core](https://github.com/allaycc/core) | The default package source. Hosts allay itself plus its foundation libs. |
| [extras](https://github.com/allaycc/extras) | Curated catalog of popular CC: Tweaked libraries (Pine3D, ecnet2, msks, ...). |
| [lualibs](https://github.com/allaycc/lualibs) | Foundation libraries: hash, pathkit, log, httpkit, argparse, levenshtein, ui, scout. Reusable outside allay. |
| [unicornpkg-compat](https://github.com/allaycc/unicornpkg-compat) | Translator for installing unicornpkg-format packages through allay. |
| [spec](https://github.com/allaycc/spec) | Versioned format specs: package definition, source index, lockfile. |
| [server](https://github.com/allaycc/server) | Serve allay packages over rednet (experimental). |
| [rednet-transport](https://github.com/allaycc/rednet-transport) | rednet:// transport plugin so clients can fetch packages from an allay-server (experimental). |
