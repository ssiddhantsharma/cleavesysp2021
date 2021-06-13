## BMSIS'21 YSP 👨‍💻👋
What we'll be doing this Summer'21 with prebiotic chemical reaction networks with [Jim](https://scholar.google.com/citations?hl=en&user=PZDaFLcAAAAJ&view_op=list_works&sortby=pubdate) Please click on hyperlinks wherever they are present to know more.

<img align="center" alt="Coder GIF" height=250 width=450 src="https://thumbs.gfycat.com/EvilNextDevilfish-small.gif"/>

### Recommended papers to read (use scihub if don't have access)
* [1](https://onlinelibrary.wiley.com/doi/abs/10.1002/wcms.1354)
* [2](https://jcheminf.biomedcentral.com/articles/10.1186/s13321-020-00456-1)

### Chemical Formats:
* Understanding what SMILES/NOL2/SDF mean and how to interconvert in between all three using either, 1) [OpenBabel](http://openbabel.org/docs/dev/Command-line_tools/babel.html) or 2) [RDKit](https://gist.github.com/leelasd/43219a222bf57d3e01c2c83f2ad9b031) whatever floats your boat! OpenBabel did mine :)  
* Play around with drawing smiles: [GDB-SMILES-Drawer](https://doc.gdb.tools/smilesDrawer/sd/example/index.html)

* Most of the molecules in the networks our group generated is either in a .smi file or a .txt file. But these are 2D representations good for most use-cases but not good for descriptor computations. How to go about it now? Get a list of smiles in a text file, download [Datawarrior](https://openmolecules.org/datawarrior/index.html) and load the smiles file in the program. You can now convert it to a sdf. Use a command-line OpenBabel for more manipulations of the SDF and read [this](http://hjkgrp.mit.edu/content/geometries-strings-smiles-and-openbabel)

### Descriptor Computations and Visualization:
* We have to calculate some **physio-chemical descriptors** for our given set of molecules. The standard way to plot them is a simple X-Y Scatter Plot (I'll provide my script so that all the plots coming out of the group remain consistent) where X = Monoisotopic Mass/Exact Mass and Y = Descriptor Value. You can calcualate the Monoisotopic Mass (keep the plot label as exact mass only) through the use of  > calculate chemical properties menu in Datawarrior. I developed the script in Seaborn-Python, you are free to choose any!
* Calculating descriptors can be done in a multitude of ways which we have tried and tested to see what works the best.
1) [PaDel](https://mordred-descriptor.github.io/documentation/master/index.html): Use the java utiility only when you have less than 10,000 molecules to calculate 2D/3D Descriptors.
2) [CDK-GUI](https://www.softpedia.com/get/Science-CAD/CDK-Descriptor-Calculator.shtml): Use the java GUI to fill in the missing descriptors with PaDel. 
3) [MORDRED](https://mordred-descriptor.github.io/documentation/master/index.html): Python Package to calculate both 2D/3D descriptors, for 3D please convert add hydrogens to your SDF at pH= 7.4 in OpenBabel. Working script for MORDRED is with us, so will share that too.
4) [PyBIOMED](https://github.com/gadsbyfly/PyBioMed): For people who are going to be playing with biological relevant data, check this out.

* Try to couple these all workflows to [Cinfony](http://cinfony.github.io/) which is an integrated package. Will reduce a lot of your repititive tasks.
* You can see these cheminformatics toolkits just to play around: [CDB Tools](http://cdb.ics.uci.edu/) and [Chemdes](http://www.scbdd.com/chemdes/)


### Gibbs Free Energy Computation and Visualization:
* We aren't going the quantum chem route for insanely computationally expensive calculations but we'll be using the [Equilibrator-API](https://equilibrator.weizmann.ac.il/) for gibbs free energy calculations at various pH's along with [JRGUI](https://github.com/curieshicy/JRgui) for additional data. Both of these processes work on Group Contribution Method. We won't be generating energies through Datawarrior/OpenBabel using a force-field because that's not something we want. We want to have ones derived from Group Contribution Methods. 

### Database Comparison and Visualization:
* We'll be all comparing our generated sdf set to existing databases such as KEGG, HMDB. We want to further match our sets to EMBDB, MetaCYC, BRENDA. The script for doing this is developed as well as the visualization one.


### Van Krev/Kendric Mass and Mass Spectra Analysis:
* We plotted these diagrams using descriptors and missed on the automated analysis of the MS spectra we had. There are automated libraries written in R that can help with this, such as [ftmsRanalysis](https://emsl-computing.github.io/ftmsRanalysis/index.html), [FTMSViz](https://wkew.github.io/FTMSViz/SRFA-plot.html). [VanKrevLocal](https://github.com/HegemanLab/VanKrevelenLocal)


## Now what if Sid was the PI instead of Dr. Jim 👨‍💻👋

### Scaffold Analysis:
* This is useful for people working on biologically relevant data such as nucleoside analogues, we'll be using packages like: [ScaffoldGraph](https://github.com/UCLCheminformatics/ScaffoldGraph), [Scaffold_Hunter](http://scaffoldhunter.sourceforge.net/) and exploring the chemical networks generated using the new [ChemSpaX](https://chemrxiv.org/articles/preprint/ChemSpaX_Exploration_of_Chemical_Space_by_Automated_Functionalization_of_Molecular_Scaffold/14617320/1)

### MORPHER: 
* I wanted to explore this package [Morpher](https://app.assembla.com/spaces/molpher/wiki) for people working in metabolism/where the products and reactants.

### Interactive Viz:
* Work with me on how we can represent the generated data better, for the smiles we'll be using the javascript library [Mols](https://github.com/chemplexity/molecules) and I wan to create a visualization for descriptors which is [TMAP](https://tmap.gdb.tools/), something which will look like this [DrugBank](https://tmap.gdb.tools/src/drugbank/drugbank.html).
If you have sufficient python experience, building TMAPs for descriptor data is one of the side projects I have. 


