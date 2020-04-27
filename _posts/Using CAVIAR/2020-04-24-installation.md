---
layout: post
title: "Installation of CAVIAR"
date: 22.04.2020 16:31:38 -0400
category: using-caviar
author: jr
short-description: How to install CAVIAR?
---

-----

The best way to get CAVIAR is to install the Anaconda package manager for Python.
Start by downloading the Python 3.x Anaconda installer on the [--> Anaconda website <--](https://www.anaconda.com/distribution/) and install it.

Once Anaconda is installed, create a new environment for CAVIAR:
```conda create -n caviar -c jr-marchand caviar ```

Activate your environment (always activate it for using CAVIAR):
```conda activate caviar ```

And that is it! CAVIAR is accessible with the ```caviar``` command, and the user interface via the ```caviar-gui``` command.

If you want to use the PyMOL functionalities for vizualising cavities, please make sure that you have a PyMOL executable accessible as ```pymol``` in the command line.
In case you do not have PyMOL yet, you can install a version (accessible in the caviar conda environment) with:
> ```conda install -n caviar -c schrodinger pymol```



**More info coming soon**


