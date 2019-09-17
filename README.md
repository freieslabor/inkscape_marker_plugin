Inkscape Marker Plugin
======================

An inkscape plugin for creating gcode for our
[Borries 320-DP marker](https://wiki.freieslabor.org/wiki/Borries-Markierer).

Based on the work of the Attraktor Hackerspace Laser Plugin
(https://github.com/attraktorhh/inkscape_laserplugin).

This repository is part of our Borries Marker Toolchain:

* [Marker API](https://github.com/freieslabor/borries-marker-api)
* [Marker Web Control](https://github.com/freieslabor/MarkerWebControl)
* Inkscape Marker Plugin (this repository)

License
-------

GPLv2 or later. See license headers in source files.

Install
-------

Put the ``attraktor_laser.py`` and ``attraktor_laser.inx`` in your inkscape
extension folder. Also put the marker template in the templates directory.

E.g. for Debian users:

    ln -s /path/to/this/git/attraktor_laser.py ~/.config/inkscape/extensions/attraktor_laser.py
    ln -s /path/to/this/git/attraktor_laser.inx ~/.config/inkscape/extensions/attraktor_laser.inx
    ln -s /path/to/this/git/marker.svg ~/.config/inkscape/templates/marker.svg

Set up Inkscape Workspace
-------------------------

File -> New from Template...

Choose "marker".

Now you have a document reflecting the actual marking area. Do not draw over the
document limits.

How To Use
----------

To create gcode select all objects that you want to mark, make sure they are
paths by clicking on "Path/Object to Path" and export with
"Extensions/Export/Attraktor Laser..."

Marking Order
-------------

In order to have stuff marked in the correct order put them on separate layers.
The layers on top of the layer list will be marked first.

Solid/Striped Objects
---------------------

There is an additional plugin called eggbot_hatch from the eggbot project
(http://egg-bot.com) included. It can put lines into closed paths - that
way you can mark "solid" or striped objects.
