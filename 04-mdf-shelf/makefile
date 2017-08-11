MESH = all.msh
SETS = bottom.nam symXZ.nam symYZ.nam top.nam
LOADS = 
PREP = pre.fbd
INP = analysis
POST = post.fbd
CPUS = 4

post: $(POST) $(INP).frd
	cgx -b $(POST)
analysis $(INP).frd: $(MESH) $(SETS) $(LOADS) $(INP).inp
	export OMP_NUM_THREADS=$(CPUS)
	ccx $(INP) &>ccx.log
$(SETS) $(LOADS) $(MESH): $(PREP)
	cgx -bg $(PREP)
pre: $(PREP)
	cgx -b $(PREP)

.PHONY: clean

clean:
	rm -f *.nam *.dlo *.frd *.sta *.dat *.cvg *.out *.msh
