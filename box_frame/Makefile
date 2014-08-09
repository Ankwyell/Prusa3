#This makefile creates stl files in output folder from scad files.



.PHONY: all

all: output/x-carriage.stl output/x-end.stl output/y-axis-bracket.stl output/y-axis-corner.stl output/y-belt-holder.stl \
output/y-drivetrain.stl output/z-axis.stl output/extras/bearing-holder-single-plate-y.stl output/extras/calibrate.stl \
output/extras/endstop-holder.stl output/extras/foldingclamp.stl output/extras/gregs-wade-v3.stl output/extras/groovemount.stl \
output/extras/tube_clamp.stl output/extras/wade-gears.stl

# explicit wildcard expansion suppresses errors when no files are found
include $(wildcard *.deps)


output/%.stl: %.scad
	unset SESSION_MANAGER ; openscad -m make -o $@ -d $@.deps $<

.PHONY: clean

clean:
	rm output/*.stl output/extras/*.stl
