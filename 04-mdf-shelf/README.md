# Deflection of a MDF shelf

MDF plate supported on 3 sides, bending from distributed load.
Planar isotropy (orthotropic material) is used. Linear static analysis.

## Files
Files:
* `pre.fbd`: Geometry, meshing and loads.
* `analysis.inp`: Material properties and supports.
* `post.fbd`: Results loading and display.

## Pre-processing
Run:
```
make pre
```
Runs pre-processing script (in batch mode) to create mesh, sets and loads definition.
## Run analysis:
Run:
```
make analysis
```
Runs ccx analysis.
## Post-processing
Run:
```
make post
```
Runs post-processing script and leaves cgx window open.
## All in one step
Run:
```
make
```
## Clean
To delete all intermediary and result files, run:
```
make clean
```
