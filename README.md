# st - simple terminal

st is a simple terminal emulator for X which sucks less.

## Requirements

In order to build st you need the Xlib header files.

## Installation

Edit config.mk to match your local setup (st is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install st (if
necessary as root):

    make clean install

## Running st

If you did not install st with make clean install, you must compile
the st terminfo entry with the following command:

    tic -sx st.info

See the man page for additional details.

## Xresources

This version supports reading some settings from Xresources. Available values are:

- font
- color0
- color1
- color2
- color3
- color4
- color5
- color6
- color7
- color8
- color9
- color10
- color11
- color12
- color13
- color14
- color15
- background
- foreground
- cursorColor
- termname
- shell
- xfps
- actionfps
- blinktimeout
- bellvolume
- tabspaces
- cwscale
- chscale
- alpha

## Non-standard ANSI sequences

This version of st supports changing the default background and foreground colors
at runtime using escape sequences. The sequences don't appear to be used anywhere
else.

### Change Default Background and Foreground Colors

Foreground ANSI sequence: `ESC 50m` - `ESC 57m`
Background ANSI sequence: `ESC 60m` - `ESC 67m`

Foreground RGB value: `ESC 58;2;r;g;bm`
Background RGB value: `ESC 68;2;r;g;bm`

### Change Default Background and Foreground Bright Colors

Foreground ANSI sequence: `ESC 110m` - `ESC 117m`
Background ANSI sequence: `ESC 120m` - `ESC 127m`

## Credits

Based on Aurélien APTEL <aurelien dot aptel at gmail dot com> bt source code.
