MESH = all.msh
SETS = bottom.nam symXZ.nam symYZ.nam
LOADS = top.dlo
PREP = pre.fbd
INP = analysis
POST = post.fbd

post: $(POST) $(INP).frd
	cgx -b $(POST)
analysis $(INP).frd: $(MESH) $(SETS) $(LOADS)
	ccx $(INP)
$(SETS) $(LOADS) $(MESH): $(PREP)
	cgx -bg $(PREP)
pre: $(PREP)
	cgx -b $(PREP)

.PHONY: clean

clean:
	rm -f *.nam *.dlo *.frd *.sta *.dat *.cvg *.out *.msh
