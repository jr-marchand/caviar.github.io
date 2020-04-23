---
layout: post
title: "Command line use"
date: 22.04.2020 16:33:38 -0400
category: using-caviar
author: jr
short-description: Batch use 
---


Once you have installed CAVIAR and activated the environment , you can call the command line instance of CAVIAR simply with:
```caviar -h```

This will trigger the presentation of the tool. The most basic use only requires a pdb code:
```caviar -code 1dwc```

#The terminal output
The output is visualized in the terminal as a table. The first table contains the list of identified cavities, ranked by cavity score. 

PDB_chain | CavID | Ligab. |  Score |  Size | Hydrophob | Interchain | AltLocs | MissAtoms
----------|--------|---------|--------|-------|-----------|------------|---------|----------
1dwc_H    |     1  |   0.6   |   3.7  | 333   |   39%     |     0      |    0    |    0     
1dwc_H    |     2  |   0.2   |   0.9  |   51  |   10%     |     0      |    0    |    0
1dwc_H    |     3  |   0.8   |   0.6  |   63  |   56%     |     0      |    0    |    0

The "H" in 1dwc_H indicates that this is the chain H of PDB code 1dwc.

Ligab. = ligandability estimator

[0.0 - 0.2] = likely hard to ligand

[0.4-0.6] = not conclusive

[0.8-1.0] = probably easy to ligand

Score = cavity score, scales with size and buriedness: the bigger and the more buried, the higher the score.

Hydrophob = hydrophobicity, count of aliphatic+aromatic grid points / total number of grid points.

Interchain = is the cavity in between two protein chains? (Boolean) Some interfaces are spurious (crystal contacts), some are productive (biological interfaces). Please keep that in mind when analysing the results.

AltLocs = Does the cavity contain residues alternate locations? (Boolean)

MissAtoms = Does the cavity contain missing atoms or residues? (Boolean) We advise to be very careful with cavities containing missing atoms, as they may be very noisy or even spurious.


#Generated files
In addition, CAVIAR generates by default a certain number of files in the working directory:

```
|-- 1dwc_cavities.pml
|-- 1dwc_subcavities.pml
|-- caviar_out/
    |-- 1dwc_cavs.pdb
    |-- 1dwc_subcavs.pdb
```


The two \*.pml files are pymol session files to automatically open and visualize the pdb file and its cavities or subcavities, respectively. The folder caviar_out/ contains the original PDB file with at the end, the cavities with the residue name GRI and the subcavities as SUB. Cavities contain as b factor the buriedness for each cavity grid point (from 8 to 14, with 14 being the most buried) and as occupancy field the pharmacophore type of the grid point, i.e., the chemical type of the closest atom of the protein. By default, the coloring of cavities is one color per cavity, but this can be changed for a coloring by buriedness or pharmacophore types, with a legend (cf hereafter). Subcavities 


#Command line arguments


```caviar``` handles both command line arguments and the use of parameter files. 


#Configuration file



