# surf - simple webkit-based browser

surf is a simple Web browser based on WebKit/GTK+.

My build of surf, the feather-weight and simple web browser made by suckless.
See the original website at [surf.suckless.org](https://surf.suckless.org)

## Features

- add/remove bookmarks (one per line in ~/.config/surf/bookmarks)
- custom search engines (prefixes)
- quick search with duckduckgo

## Applied Patches

Some patches may have been modified by me to suit my needs better.

- [bookmarking](http://surf.suckless.org/patches/bookmarking/)
- [searchengines](http://surf.suckless.org/patches/searchengines/)
- [web search](https://surf.suckless.org/patches/web-search/)

## Requirements

In order to build surf you need GTK+ and Webkit/GTK+ header files.

In order to use the functionality of the url-bar, also install dmenu[0].

## Installation

Edit config.mk to match your local setup (surf is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install surf (if
necessary as root):

    make clean install

To keep things tidy, some features depend on the existence of external scripts in PATH.
These scripts follow the "surf-script-*" naming convention, you can install them by
symlinking to /usr/local/share with this one-liner (execute from the repo root directory):

    find . -maxdepth 1 -name "surf-script-*" -print0 | xargs -0 -I % sudo ln -sTf -- "$(realpath -- "%")" "/usr/local/bin/$(basename -- "%")"

## Running surf

run
	surf [URI]

See the manpage for further options.

## Running surf in tabbed

For running surf in tabbed[1] there is a script included in the distribution,
which is run like this:

	surf-open.sh [URI]

Further invocations of the script will run surf with the specified URI in this
instance of tabbed.

[0] http://tools.suckless.org/dmenu
[1] http://tools.suckless.org/tabbed

