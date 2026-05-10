# allay

allay is the only package manager that actually manages packages for [CC: Tweaked](https://tweaked.cc).

as expected, it makes CC software easier to install, uninstall, update and publish.

it makes ANY CC software easier to install. And we work with unicornpkg packages too!

#### bring a package, a repo, a library, or a pile of Lua files. allay will try to make sense of it.

for users, that means less copying files around and less chasing missing libraries.

for developers, that means you can ship software without writing a custom installer for every project.

## install:

```sh
wget run https://raw.githubusercontent.com/allaycc/allay/main/install.lua
```

> ideally, this is the last installer you paste by hand.

## built for the CC ecosystem that already exists

most CC projects were not written for a package manager. allay is built around that.

allay can install from package sources, existing package formats, and github repos directly. if a repo has package metadata, great! allay will use it. if it does not, allay can still inspect the project, read code, find installable files, and build an install plan where possible.

the goal is to make CC software installable wherever it already lives.

## for users

install the allay or unicornpkg repo you want:

```sh
allay install package
```

or install **any other** CC software from github:

```sh
allay install gh:user/repo
```

unicornpkg packages work too

if a package is already in unicornpkg format, allay can read it through the compatibility layer 'alicorn': 

```sh
allay info alicorn
```

update everything later:

```sh
allay update
```

remove what you no longer need:

```sh
allay remove package
```

## dependencies

you install a program, it complains about a missing library, you go find that library, and then maybe that library needs something else.

allay makes that trivial.

if a package declares dependencies, allay installs them automatically. if a github repo uses libraries allay recognizes, it can pull those in too. if something cannot be resolved automatically, allay tells you what it couldn't find.

shared dependencies are installed once and reused by the packages that need them.

## updates

allay remembers where installed packages came from.

```sh
allay update
```

normal packages update from their source, and github repo installs can refresh from the repo they came from.

you can update everything at once, or update one package:

```sh
allay update package
```

## for developers

publishing CC software should not be harder than writing it.

with allay, you can make a project installable by adding package metadata and publishing it through a source.

```sh
allay init
```

a package can include programs, libraries, startup files, config files, help files, and dependencies. allay puts them where they belong, and users get a normal install/update/remove flow.

## package sources

allay does not depend on one central catalog.

```sh
allay source add user/repo
allay source add https://example.com/packages
```

sources can be GitHub repos, https hosts, floppy disks, or even rednet transports with the plugin installed.


## repos

| repo | what it is |
|---|---|
| [allay](https://github.com/allaycc/allay) | cli and runtime |
| [core](https://github.com/allaycc/core) | default package source |
| [extras](https://github.com/allaycc/extras) | curated CC: Tweaked libraries and tools |
| [lualibs](https://github.com/allaycc/lualibs) | reusable lua libraries used by allay |
| [alicorn](https://github.com/allaycc/alicorn) | unicornpkg compatibility |
| [spec](https://github.com/allaycc/spec) | package, source index, and lockfile specs |
| [server](https://github.com/allaycc/server) | experimental rednet package server |
| [rednet-transport](https://github.com/allaycc/rednet-transport) | experimental `rednet://` transport |
