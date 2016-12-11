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
extension folder.

E.g. for Debian users: ~/.config/inkscape/extensions/

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
way you can laser solid black or striped objects.
