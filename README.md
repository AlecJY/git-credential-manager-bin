# Git Credential Manager binary package for MSYS2

[![build result](https://build.opensuse.org/projects/home:AlecJY:msys2/packages/git-credential-manager-bin/badge.svg?type=default)](https://build.opensuse.org/package/show/home:AlecJY:msys2/git-credential-manager-bin)

---

## Installation
### Download manually
Download the latest version from [release page](https://github.com/AlecJY/git-credential-manager-bin/releases)

Then use the command below to install
``` bash
$ pacman -U git-credential-manager-bin-*-any.pkg.tar.xz
```

### Install from the repo (Experimental)
Follow the [instruction](https://software.opensuse.org//download.html?project=home%3AAlecJY%3Amsys2&package=git-credential-manager-bin)

## Packaging
Use the following commands to package Git Credential Manager by yourself
```bash
$ git clone https://github.com/AlecJY/git-credential-manager-bin.git
$ cd git-credential-manager-bin
$ makepkg
```
