st - simple terminal
--------------------
st is a simple terminal emulator for X which sucks less.


Note
------------
My build of st for Arch Linux, Void Linux, Gentoo Linux, FreeBSD, and OpenBSD. 

Used patches are in `patches/done/` directory.

Requirements
------------
In order to build st you need the Xlib header files.

On Void and FreeBSD you might need to install some required pkgs before building.
See this [README](https://github.com/Linerre/dwm/blob/arch/README.md)

Also, to build st on FreeBSD, you need to install `ncurses`:

	# pkg install ncurses

`ncurses` contains the `tic` program. 

Installation
------------
Edit config.mk to match your local setup (st is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install st (if
necessary as root):

    make clean install


Running st
----------
If you did not install st with make clean install, you must compile
the st terminfo entry with the following command:

    tic -sx st.info

See the man page for additional details.

Credits
-------
Based on Aurélien APTEL <aurelien dot aptel at gmail dot com> bt source code.

