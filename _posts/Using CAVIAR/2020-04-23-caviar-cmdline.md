---
layout: post
title: "Command line use"
date: 22.04.2020 16:33:38 -0400
category: using-caviar
author: jr
short-description: Batch use 
---

Once you have installed CAVIAR and activated the environment ([reminder]({% post_url /Using CAVIAR/2020-04-22-instalation.md %})), you can call the command line instance of CAVIAR simply with:
```caviar -h```

This will trigger the presentation of the tool. The most basic use only requires a pdb code:
```caviar -code 1dwc```

Now let us look at the output. The first part is a table containing the list of identified cavities, ranked by cavity score. 

PDB_chain | CavID | Ligab. | Score | Size | Hydrophob | Interchain | AltLocs | MissAtoms
----------|-------|--------|-------|------|-----------|------------|---------|----------
1dwc_H    |    1  |  0.6   |  3.7  | 333  |   39%     |     0      |    0    |    0     
1dwc_H    |    2  |  0.2   |  0.9  |  51  |   10%     |     0      |    0    |    0
1dwc_H    |    3  |  0.8   |  0.6  |  63  |   56%     |     0      |    0    |    0



In addition, CAVIAR generates by default a certain number of files in the working directory:

> .
> |-- 1dwc.pdb (if it needs to download the file, cf hereafter)
> |-- 1dwc_cavities.pml
> |-- 1dwc_subcavities.pml
> |-- caviar_out/
>     |-- 1dwc_cavs.pdb
>     |-- 1dwc_subcavs.pdb


```caviar``` handles both command line arguments and the use of parameter files. 


**This article is coming soon**

