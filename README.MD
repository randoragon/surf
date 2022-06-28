# surf - simple webkit-based browser

surf is a simple Web browser based on WebKit/GTK+.

My build of surf, the feather-weight and simple web browser made by suckless.
See the original website at [surf.suckless.org](https://surf.suckless.org)

## Features

- add/remove bookmarks (one per line in ~/.config/surf/bookmarks)
- custom search engines (prefixes)
- search in duckduckgo by prefixing a query with '\`'
- use XA\_CLIPBOARD instead of XA\_PRIMARY for C-y and C-p operations
- spawn download history in a terminal with <C-S-d>
- edit page source in $EDITOR
- follow links with keyboard shortcuts + dmenu

## Applied Patches

Some patches may have been modified by me to suit my needs better.

- [bookmarking](http://surf.suckless.org/patches/bookmarking/)
- [searchengines](http://surf.suckless.org/patches/searchengines/)
- [spacesearch](http://surf.suckless.org/patches/spacesearch/)
- [dlconsole](https://surf.suckless.org/patches/dlconsole/)
- [externalpipe](https://surf.suckless.org/patches/externalpipe/)
- [quit hotkey](https://surf.suckless.org/patches/quit-hotkey/)

## Requirements

In order to build surf you need GTK+ and Webkit/GTK+ header files.

In order to use the functionality of the url-bar, also install dmenu[0].

## Installation

Edit config.mk to match your local setup (surf is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install surf (if
necessary as root):

    make clean install

## Running surf

run
	surf [URI]

See the manpage for further options.
