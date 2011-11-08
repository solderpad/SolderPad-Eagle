SolderPad Eagle
===============
A set of scripts to assist adding a [Cadsoft Eagle](http://www.cadsoftusa.com/eagle-pcb-design-software/?language=en) project to [SolderPad](SolderPad.com)

Open an the .sch file in Eagle, and run one of the scripts from the File->Script dialog.

Alternatively, copy the scripts into the Eagle/ulp directory and run them from the command-line:

	$ cd .solderpad
	$ eagle -C'RUN bom-json.ulp; QUIT;' ../myproject.sch

You might also like to generate the schematic and board images from the command-line:

	$ eagle -C'EXPORT IMAGE schematic.png 600;QUIT' ../*sch
	$ eagle -C'EXPORT IMAGE board.png 600;QUIT' ../*brd

It's possible to incorporate these scripts into Makefile or run as a git hook so the export is run automatically beofore pushing to SolderPad.
