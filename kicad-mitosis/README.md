Kicad Mitosis
=============

A port of original Mitosis converted with [altium2kicad](https://github.com/thesourcerer8/altium2kicad).

Disclaimer
----------

NEITHER OF THOSE LAYOUTS WERE ACTUALLY CHECKED IN PRODUCTION, USE AT YOUR OWN RISK!

* default - cleaned up autoconverted version, should be ready for export
* YJ-14015-support - wider pads for YJ-14015 (still a bit unfinished check pads carefully!)
* autoconverted - raw autoconverted board (misplaced labels, messed up outlines, etc.)

Mind that there's no network yet so it couldn't be autorouted.

Converting
----------

Apply .pl scripts then delete all unnecessary Edge.Cuts (such as 10x10 cm outline).

Remove board outline from Dwgs.User.

All footprint texts made invisible ("Switch", "NRF51822", etc. - they weren't in the gerbers).

Battery footprint and mitosis branding will appear misplaced, so move them down.

Check results in 3D viewer against the original gerber.

Editing
-------

To make bigger nrf51 pads, use select - Edit All Pads, set width to 2.5 mm and apply for all.


Exporting
---------

Use File-Plot command to export gerber files.

Check F.Cu, B.Cu, B.Paste, F.Paste, B.Silk, F.Silk and the Edge.Cuts layers, and also Dwgs.User.

Do not check Exclude PCB edge layer from other layers.

Then export Drill file, use Gerber in the Format section and check Minimal header.






