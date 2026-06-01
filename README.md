# `The Linux Kernel`

This is a for of the Linux kernel repository to play with experimental kernel patches that I need.
Nothing of importance really, just ignore it.

Work is in branches, I typically keep only 2 working branches,
the last released kernel, and the last `-rc` kernel (`torvalds/master`).

## QuickStart

Kernel config is saved with:
```
make savedefconfig
```
We can then copy/move the created `defconfig` file somewhere else.

To restore from a `defconfig` run:
```
mv defconfig arch/x86/configs/my_defconfig
make my_defconfig
```

### ArchLinux package

```
make -j $(nproc) PACMAN_PKGBASE=linux-git PACMAN_EXTRAPACKAGES="" pacman-pkg
sudo pacman -U ./linux-git-…
```
