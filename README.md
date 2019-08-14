# simplelock
Fast and simple wrapper over i3lock with multiple modes.

Updates to your lockscreen happen in the background while 
your machine is locked, and appear the next time you lock your screen.

## Sample

![sample](sample.png)

## Usage

`simplelock <mode>`

### Available modes

#### `unsplash`: fetches a random wallpaper from unsplash

Usage:

`simplelock unsplash <resoultion> <query>`

Example:

`simplelock unsplash 1920x1080 nature,buildings`

#### `xkcd_latest`: fetches the latest xkcd comic and tiles it 

Example:

`simplelock xkcd_latest`

#### `xkcd_random`: fetches random xkcd comic and tiles it

Example:

`simplelock xkcd_random`

#### `custom_fetch`: fetch image from any url

Example: 

`simplelock custom_fetch https://my.domain/image.png`

#### `custom_file`: use any image available locally

Example: 

`simplelock custom_file ~/Pictures/wallpapers/current.png`

## Installation

simplelock is a drop in replacement for i3lock. 

If you are using i3wm you can edit your i3 config file and 
replace i3lock/blurlock etc with simplelock.

For Manjaro i3, you might have to edit the `i3exit` script that
is bundled.

You can install it from source or the Arch User Repository.

### AUR

Simple lock is available in the [AUR](https://aur.archlinux.org/packages/simplelock/).

## Manual Install

```bash
set -e
git clone git@github.com:rhnvrm/simplelock.git
cd simplelock
mkdir -p ~/.config/simplelock
cp lock.png ~/.config/simplelock/
cp lockscreen.png ~/.config/simplelock/
install -D -m755 -t "/usr/bin" "simplelock"
```

## Caveats

### XFCE

- Running simplelock with `Super+L` might fail to lock in certain cases on 
XFCE with the whisker menu bound to open with `Super`. This is because of
a known issue, you can read more about it [here](https://forum.manjaro.org/t/xfce-super-win-key-shortcut-problem/51797/3). It suggests using `xcape` from the Manjaro Community repo instead of `ksuperkey`, which resides in the AUR.