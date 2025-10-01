# Setup and preliminary stuff
Recommended: Install the full Anaconda Distribution.
If you run into problems, are working on weird hardware, or have too little diskspace, you can also try Miniconda.

## Anaconda (Recommended)
- Follow steps described [here](https://www.anaconda.com/docs/getting-started/anaconda/install).
- Go to [Anaconda Downloads](https://www.anaconda.com/download/) and download and install Anaconda.
- Start up the [conda navigator](https://www.anaconda.com/docs/tools/anaconda-navigator/getting-started), and start the jupyter server.

### Anaconda Navigator
- Open the Environments tab on the left side, select the base environment.
- Click on channels and add `conda-forge` (see [example](https://docs.anaconda.com/_images/nav-add-channel1.gif)).
- See [Navigator getting started](https://docs.anaconda.com/navigator/getting-started/) and [Managing Environments Tutorial](https://docs.anaconda.com/navigator/tutorials/manage-environments/).

### Test your setup
- Start the Anaconda Navigator.
- Click the launch button below Jupyter.
- Run the `notebooks/00_jupyter_hello_world.ipynb` in Browser (from here on everything is the same, no matter if Miniconda or full Anaconda is installed)
- Using jupyter in Browser, navigate to the location where you extracted the zip file and double click on the ipynb file.


## Advanced (stuff you only need when running mini conda or want to dig deeper)
### Notebook support in Spyder (if you want to use spyder)
You can either use Anaconda Navigator or the Anaconda Prompt:

### Using the Anaconda Prompt
Open an Anaconda Prompt (either search for it in your start menu, or open via start page of the Anaconda Navigator).
Run the following command:
```bash
conda install spyder-notebook -c conda-forge
```

### Mini Conda (If for some reason you have too little HDD space, or run into other problems)
Go to [Conda Website](https://docs.conda.io/projects/conda/en/latest/user-guide/install/index.html) and install Miniconda.

#### Test your mini conda setup
- Open a Miniconda prompt (from start menu). (or open a regular cmd shell and run `conda activate base`).
- Run `jupyter notebook` in the prompt and your browser should open the Jupyter start screen. (If it doesnt, scroll up the shell output and find the line with the url http://localhost:8888 ...)
- Run the `notebooks/00_jupyter_hello_world.ipynb` in Browser (from here on everything is the same, no matter if Miniconda or full Anaconda is installed)
- Using jupyter in Browser, navigate to the location where you extracted the zip file and double click on the ipynb file.

### Activate environment
```bash
conda activate base
```

### Install dependencies we will need in this course
```bash
conda install anaconda::spyder anaconda::pandas anaconda::scikit-learn anaconda::matplotlib
conda install spyder-notebook -c conda-forge
conda install conda-forge::pytest
conda install anaconda::parameterized 
conda install anaconda::seaborn 
```

### IDEs
- Jupyter in Browser (recommended)
- [Spyder](https://www.spyder-ide.org/) (recommended, already comes with Anaconda)
- [PyCharm](https://www.jetbrains.com/pycharm/) (recommended, free pro versions for students, Jupyter Notebook support only in pro version) 
- [VSCode](https://code.visualstudio.com/)


## Test your conda setup
### Using Anaconda install
Start the Anaconda Navigator.
Click the launch button below Jupyter.

# FAQ
## Im running a Mac and Anaconda installation fails or Anaconda doesnt start.
Find out what MacBook you are using, google what processor architecture it has (intel, arm), and download the correct Anaconda installer and try again.
If that doesnt work, try to install Miniconda.

## Im running Windows 7
Update to a newer Windows version, or install a lightweight linux distro parallel to your Windows OS (I can recommend [Linux Mint](https://www.linuxmint.com/) for first time users coming from Windows).

## I dont have a notebook tab in spyder (but you want to use spyder).
Redo the steps described above in 'Notebook support in Spyder'.
If you are running Anaconda and installation using Anaconda Navigator doesnt work, use the above described way via the Anaconda Prompt.

## How do I open a notebook in spyder?
Go to the Notebook tab (bottom center of the editor window), and then click on the button with the three vertical bars in the top right corner of this window [Example](https://docs.spyder-ide.org/current/_images/notebook-open.gif).
