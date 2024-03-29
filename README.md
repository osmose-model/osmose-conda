# Osmose Conda environments 

In order to easily install all the tools to compile and run Osmose, install Anaconda (https://www.anaconda.com/products/individual). 

**Note: using conda environments, the use of RStudio is not guaranteed. It can be used to install Osmose-compatible environments on HPC servers.**

## Anaconda install

### Linux users

When downloaded, run the install script as follows:

```
bash Anaconda3-2020.11-Linux-x86_64.sh
```

**Do not allow the `git-init` command**. 

When done, add the following line to your `~/.bash_profile` and `~/.bashrc` files:

```
. $CONDA/etc/profile.d/conda.sh
```

with `$CONDA` the path of your `Anaconda` install. 

### Mac Os X users

When downloaded, double-click on the ```Anaconda3-2020.11-MacOSX-x86_64.pkg``` file. 

When done, add the following line to your `~/.bash_profile` and `~/.bashrc` files:

```
. $CONDA/etc/profile.d/conda.sh
```

with `$CONDA` the path of your `Anaconda` install.

### Windows users

Double-click on the ```Anaconda3-2020.11-Windows-x86_64.exe``` and follow the install instructions. 

## Install Osmose Environments

### From command line (Anaconda Prompt, Terminal)

- Open a Terminal or the Anaconda prompt, and type: `conda create -c conda-forge --name osmose`
- Activate the environment: `conda activate osmose` 
- Install the Osmose and CalibraR related packages by typing:
```
conda install -y r r-ncdf4 r-knitr r-rmarkdown r-stringr r-rlist r-fields r-mgcv maven r-devtools r-r.utils r-cmaes r-optimr r-dosnow r-snow r-doparallel
```
- To build the documentation, install the Sphinx related packages:
```
conda install -y matplotlib sphinxcontrib-programoutput sphinxcontrib-bibtex ipython sphinx_rtd_theme pandas
```
- In order to use Jupyter notebooks, in association with the Jupytext extension, install the Jupyter related packages:
```
conda install -y r-irkernel
```

**Note: your `base` environment must contain the `nb_conda_kernels` package.**

- To use Visual Studio Code R extension: 
```
conda install -y r-languageserver
```

- **For Windows users**, type: `conda install -y rtools`

### From Anaconda Navigator (Windows/MacOs users)

- Open the `Anaconda Navigator`
- Click on `Environments` and on the `Create` button. Select `R` and deselect `Python`
- In the `Channels` box, make sure that both `Defaults` and `Conda-Forge` are available.
- Select all the packages listed in the above and which are not installed yet, then click on `Apply`
