# Git Credential Manager Core binary package for MSYS2

## Installation
Download the latest version from [release page](https://github.com/AlecJY/git-credential-manager-core-bin/releases)

Then use the command below to install
``` bash
$ pacman -U git-credential-manager-core-bin-*-any.pkg.tar.xz
```

## Packaging
Use the following commands to package Git Credential Manager Core by yourself
```bash
$ git clone https://github.com/AlecJY/git-credential-manager-core-bin.git
$ cd git-credential-manager-core-bin
$ makepkg
```
