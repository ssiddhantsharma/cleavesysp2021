## BMSIS'21 YSP 👨‍💻👋
What we'll be doing this Summer'21 with prebiotic chemical reaction networks with [Jim](https://scholar.google.com/citations?hl=en&user=PZDaFLcAAAAJ&view_op=list_works&sortby=pubdate)  

### Chemical Formats:
* Understanding what SMILES/NOL2/SDF mean and how to interconvert in between all three using either, 1) [OpenBabel](http://openbabel.org/docs/dev/Command-line_tools/babel.html) or 2) [RDKit](https://gist.github.com/leelasd/43219a222bf57d3e01c2c83f2ad9b031) whatever floats your boat! OpenBabel did mine :)

* Most of the molecules in the networks our group generated is either in a .smi file or a .txt file. But these are 2D representations good for most use-cases but not good for descriptor computations. How to go about it now? Get a list of smiles in a text file, download [Datawarrior](https://openmolecules.org/datawarrior/index.html) and load the smiles file in the program. You can now convert it to a sdf. Use a command-line OpenBabel for more manipulations of the SDF and read [this](http://hjkgrp.mit.edu/content/geometries-strings-smiles-and-openbabel)

### Descriptor Computations and Visualization:

