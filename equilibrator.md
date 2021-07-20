### There are some problems installing the different equilibrator packages via pip. So you end up having to just download certain repos from gitlab and install using the local versions. 

1) Notes on installing equilibrator v4.0 version of equilibrator assets on a conda virtual environment (eq4)
followed instructions here to make new conda environment "eq4" https://conda.io/projects/conda/en/latest/user-guide/getting-started.html

2) Activated, and checked to make sure that calling python3 searched in the eq4 directory by doing which -a python3

3) Follow "alex_danielssen" answer here to install packages: 
https://stackoverflow.com/questions/41060382/using-pip-to-install-packages-to-anaconda-environment

``` python -m pip install <package> ```

4) using local_compound_cache_zenodo branch of kevin's gitlab here: https://gitlab.com/KShebek/equilibrator-assets/-/blob/local_compound_cache_zenodo/notebooks/local_cache.ipynb

5) Open babel installed just fine using the command conda install -c conda-forge openbabel BUT equilibrator-assets would NOT install over pip. So we had to install by downloading and extracting the zip of the repo, then doing: 
````python3 -m pip install -e equilibrator-assets-master/ ````

The conda environment can be added to jupyter by following the instructions here: https://medium.com/@nrk25693/how-to-add-your-conda-environment-to-your-jupyter-notebook-in-just-4-steps-abeab8b8d084

```` conda install -c anaconda ipykernel ```` then

```` python3 -m ipykernel install --user --name=firstEnv ````
