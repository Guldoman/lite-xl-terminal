# lite-xl-terminal

`lite-xl-terminal` is a (mostly) fully-featured terminal emulator designed to slot into lite-xl as a plugin for windows, mac and linux.

## Installation

The easiest way to install `lite-xl-terminal` **will be** to use [`lpm`](https://github.com/lite-xl/lite-xl-plugin-manager), and
then run the following command:

```
lpm install terminal
```

If you want to simply try it out, you can use `lpm`'s `run` command:

```
lpm run terminal
```

Because we're not released yet, this won't work yet, so you'll have to build the thing manually,
and copy it into lite like so:

```
git clone --depth=1 https://github.com/adamharrison/lite-xl-terminal.git --recurse-submodules --shallow-submodules
  cd lite-xl-terminal && ./build.sh && cp -R plugins/terminal ~/.config/lite-xl/plugins && cp libterminal.so ~/.config/lite-xl/plugins/terminal
```

Until we're released.

## Status

Currently pre-release. Still has major issues. Use at your own risk. See TODO, below.

Target release date is August 1st, 2023.

### Supported Shells

The following shells are tested on each release to ensure that they actually function:

* bash (Linux/Mac)
* dash (Linux/Mac)
* zsh (Linux/Mac)
* cmd.exe (Windows)

## Description

A simple, and straightforward terminal that presents itself as `xterm-256color`. Supports:

1. A configurable-length scrollback buffer.
2. Alternate buffer support for things like `vim` and `htop`.
3. Configurable color support.
4. Signal characters.
5. Configurable shell.
6. Selecting from terminal.
7. Copying from terminal.
8. UTF-8 support.
9. Terminal resizing.

Ships with bash, for windows; assumes that Mac and Linux already have bash.

## TODO

* Ensure that locked scrollback regions work correctly. (Hard)
* Windows support. (Hard)
* Expanding escape code handling. (?)
