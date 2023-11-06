# Neptune-4-Max---printer.cfg-and-other-macros
My Neptune 4 Max printer.cfg with many teaks/additions
There are quite a lot of comments etc to detail what is what. I keep everything inside the printer.cfg, with no external macro calls, so it is all self-contained.

There MIGHT be some values you need to change to suit your N4max (eg sensorless homing sensitivity) but I think it would be pretty well right for any printer.
The Input Shaping is obviously from mine, so that is something best re-done for your own. And your Bed Mesh.

I use a "BED60" mesh name, soo it is only altered when I specifically do that. There is a macro to run that and save it as that name (macro "Bed_Mesh_60"), so run that to create your BED60.

The PRINT_START is not really used. I use START_PRINT !  But still have a blank PRINT_START macro because it will call that (whether you yourself did or not!).
The reason to change that is because PRINT_START is automatically called by the Klipper system (Elegoo setup doing htat?) and if you call PRINT_START, such as from your slicer, it will be run then, but then again later by the Elegoo(?) call of it. Thus using a different name assures you call yours (START_PRINT) and they only call the BLANK version of PRINT_START.
The same is done for PRINT_END (END_PRINT), though I don't think that has the 'double call' issue really.

My printer.cfg changes reasonably often. Sometimes tweaking values. Sometimes adding macros. Sometimes editing a prior added maco. So I will try to keep this updated, but for any given current working printer.cfg it should just keep working fine as it is anyway.

If you have any issues using it, you can let me know and I can probably work out what is amiss in your setup.

You need to set the SLICER up to suit the printer - such as the bed dimensions (new values used), and the Start and End G-Code scripts.
There is a Slicer.txt file which lists the Slicer things required.
