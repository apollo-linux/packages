# Apollo Packages
Collection of Arch Linux packages primarily built for [Apollo](https://github.com/apollo-linux/apollo).

## Using the repository

In order to install packages from this repository via `pacman`, you need to import the signing key:

```bash
pacman-key --init
pacman-key --recv-key F74289FDFA6BBD5C2995DDAD8048C7731FE274FA --keyserver keyserver.ubuntu.com
pacman-key --lsign-key F74289FDFA6BBD5C2995DDAD8048C7731FE274FA
```

And add the following to `/etc/pacman.conf`:
```ini
[bootc]
SigLevel = Required
Server = https://github.com/apollo-linux/packages/releases/download/$repo
```

Afterwards, sync your repositories with `pacman -Sy`, and then install a package like so:

```bash
pacman -S xdg-terminal-exec
```

## Credits
This repo is heavily based on [hecknt/arch-bootc-pkgs](https://github.com/hecknt/arch-bootc-pkgs).