
Debian
====================
This directory contains files used to package trustplusd/trustplus-qt
for Debian-based Linux systems. If you compile trustplusd/trustplus-qt yourself, there are some useful files here.

## trustplus: URI support ##


trustplus-qt.desktop  (Gnome / Open Desktop)
To install:

	sudo desktop-file-install trustplus-qt.desktop
	sudo update-desktop-database

If you build yourself, you will either need to modify the paths in
the .desktop file or copy or symlink your trustplus-qt binary to `/usr/bin`
and the `../../share/pixmaps/trustplus128.png` to `/usr/share/pixmaps`

trustplus-qt.protocol (KDE)

