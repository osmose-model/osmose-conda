# Osmose Conda environments 

In order to easily install all the tools to compile and run Osmose, install Anaconda (https://www.anaconda.com/products/individual).

## Anaconda install

### Linux users

When downloaded, run the install script as follows:

```
bash Anaconda3-2020.11-Linux-x86_64.sh
```

**Do not allow the `git-init` command**. 

When done, add the following line to your `~/.bash_profile` file:

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

### Linux / Mac Os X users

- Open a Terminal, and navigate to the location of the Osmose `yaml` file.
- Type `conda env create -f osmose-arch.yml`, replacing `arch` by your architecture.
- When done, type `conda activate osmose`.

### Windows Users

- Open the `Anaconda Navigator`
- Click on `Environments`
- Click on the `Import` button.
- Navigate to the `osmose-windows.yml` file
- When done, select the `osmose` environment.
