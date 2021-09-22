# Osmose Conda environments 

In order to easily install all the tools to compile and run Osmose, install Anaconda (https://www.anaconda.com/products/individual).

## Anaconda install

### Linux users

When downloaded, run the install script as follows:

```
bash Anaconda3-2020.11-Linux-x86_64.sh
```

**Do not allow the `git-init` command**. 

When done, add the following line to your `~/.bash_profile` and `.bashrc` file:

```
. $CONDA/etc/profile.d/conda.sh
```

with `$CONDA` the path of your `Anaconda` install. 

### Mac Os X users

When downloaded, double-click on the ```Anaconda3-2020.11-MacOSX-x86_64.pkg``` file. 

When done, add the following line to your `~/.bash_profile` file:

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
- Install the packages by typing:
```
conda install -y r rstudio r-ncdf4 r-knitr r-fields r-rmarkdown r-stringr r-rlist r-fields r-mgcv maven
```
- **For Windows users**, type: `conda install -y rtools`
- Before compiling, running and opening Rstudio, activate the Osmose environment as follows: `conda activate osmose`

### From Anaconda Navigator (Windows/MacOs users)

- Open the `Anaconda Navigator`
- Click on `Environments` and on the `Create` button. Select `R` and deselect `Python`
- In the `Channels` box, make sure that both `Defaults` and `Conda-Forge` are available.
- Select all the packages listed in the above and which are not installed yet, then click on `Apply`
- Run RStudio from the `Home` of your newly created environment.
