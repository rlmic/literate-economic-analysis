<p align="right">
<img src="https://i0.wp.com/www.bitss.org/wp-content/uploads/2019/03/CEGA-logo-RGB-300-dpi-colour.png?ssl=1" data-canonical-src="https://www.bitss.org" width="260" height="120" />
</p>


<h1 align="center">

<b>Literate Economic Data Analysis </b>

</h1>

<h2 align="center">

<b>Computation Notebooks</b>

</h2>

<p> <br /> </p>
<p> <br /> </p>



<h3 align="center">
Daniela Pinto Veizaga
</h3>

<p align="center">
University of California, Berkeley
</p>
<p align="center">
CEGA
</p>

<p> <br /> </p>
<p align="center">
<img src="https://bitss.github.io/ACRE/BITSS_logo_horizontal.png" data-canonical-src="https://www.bitss.org" width="210" height="90" />
</p>

<div align="justify">

## 0. :wave: Introduction

Computation notebooks have become a successful mechanism for prototyping and writing examples to showcase a piece of software, sharing data analysis and documenting research workflows. The Literate Economic Data Analysis (LEDA) workshop is a hands-on tutorial[^1] through which we will learn how notebooks can complement the science and methodological development of social science research.
</div>

<p align="center" width="100%">
    <img src="https://edsbook.org/_images/notebook-cycle.jpg" width="80%" height="410" />
</p>

<p align="center">
Source: The Turing Way project. Illustration by Scriberia as part of The Turing Way book dash in November 2022. Zenodo. http://doi.org/10.5281/zenodo.7587336
</p>

### Who is this workshop for?
<div align="justify">
This workshop is designed for those who want to take their data analysis skills and expertise in Stata and potentiate them with computation notebooks. Jupyter notebook is one such form of interactive computing environment that offers multilingual programming language support to create dynamic and static documents, books, presentations, blogs, and resources. 

The workshop will introduce you to create static documents with Jupyter notebooks, add interactivity to them and integrate them with your regular workflow in Stata, translating code, widgets, narrative text, equations, and graphical objects into one working, collaborative, interactive and reproducible document.
</div>


### What we will cover?
<div align="justify">
The curriculum lays out the importance of reproducibility ◊in the context of economic data analysis, and providing an overview of the common concepts, tools and resources. We assume atendees are familiar to version control, testing, and reproducible computational environments. We build on these core concepts, to boost our data analysis skills integrating Jupyter Notebooks, Python and Stata.

The curriculum is as follows:

1. [ Background. ](#back)
2. [ Prerequirements. ](#preq)
3. [ Setup Instructions. ](#setup)
4. [ Kick-off. ](#kick)
5. [ Miscellaneous. ](#misc)
</div>

<a name="back"></a>
## 1. Background

<div align="justify">
The name of this workshop is inspired in Donald Knuth's conceptual use of literate programming, defined as a script, notebook, or computational document that contains an explanation of a program's logic in a natural language, with snippets of macros and source code, which can be compiled and rerun. An executable paper!

As economists we draw on a handful of statistical softwares, such as Stata, R, and Python, to implement our econometric analysis. Regarless of our software preferance, it is in our best interest to ensure our analyses are reproducible, properly documented and executable.

Jupyter notebooks, as well as other computation notebooks such as RMarkdowns, are heavily used in data science, because of it's interoperability with multiple programming languages --Julia, Python, R, SQL, bash, and Stata! Incorporating results directly into your documents is an important step in reproducible research.
Jupyter notebooks can be comprised mainly of three types of cells (though more can be added with plugins):

+ [Markdown cells](https://daringfireball.net/projects/markdown/syntax):  Text can be added to Jupyter Notebooks using this type of cells. Markdown is a popular markup language that is a superset of HTML. 

+ Code Cells: Allow users to edit and write code, with full syntax highlighting and tab completion. The programming language you use depends on the kernel, and the default kernel runs Python. The results that are returned from this computation are then displayed in the notebook as the cell’s output.

+ Raw cells: Provide a place in which you can write output directly. Raw cells are not evaluated by the notebook.



<a name="preq"></a>
## 2. Prerequirements

<div align="justify">
To adequately follow the workshop, you must fulfill several requirements. Please take sometime before our workshop to fulfill them:

+ Install Python and Stata in your machine,
+ Some experience working with the command line,
+ Create a GitHub account,
+ Familiarize yourself with version control.


### 2.1. Command Line or CLI


The command line interface allows users to type text commands instructing the computer to do specific tasks, instead of clicking around. Most operating systems come with a graphical user interface (GUI), enabling us to see things on our screens and click around.
</p>


Compared to a visually attractive GUI, the command line is less user friendly --initially! However, as we perform more data intensive tasks, the CLI is a powerful and vital resource because it exploits less computational resources and is highly efficient for performing repetitive tasks.

### 2.2. Python


The Python ecosystem consists of a lot of software packages that bring extended functionality and high productivity straight away. There are multiple ways to install Python, either using Anaconda or installing it directly in your computer. Anaconda is highly recommended for beginners.

+ Install Python in macOS

As a macOS user, you probably have Python installed on your system already. To check if it's installed, open your CLI and type:

```bash
python --version
```

If not installed, you can install Python with Homebrew, a package installer. First, install Homebrew.

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```

Then, install brew to path:

```bash
$export PATH="/usr/local/opt/python/libexec/bin:$PATH"
```

Next, install Python.

```bash
brew install python
```

For other operating systems, please refer to the resources available at the end of this document.


### 2.3. [Github](https://github.com)

GitHub is a code hosting platform for version control and collaboration, widely use to store and share code, track changes, and collaborate on projects with others. To start using GitHub, you need to create an account.

### 2.4. [Stata](https://www.stata.com/install-guide/)

Adquire your Stata license and install it your computer. Stata's website is comprehensive in terms of the steps needed to install Stata.

<a name="setup"></a>
## 3. Setup Instructions

### 3.1. Clone repository

To start working on your code locally or remotely, you need to clone the repository. To do this, click on the green “Code” button and copy the URL. Then, open up your terminal (or command prompt on Windows) and navigate to the directory where you want to store your code. In the command line type:

```{bash}
git clone https://github.com/rlmic/literate-economic-analysis.git
```

### 3.2. Install required packages

#### Jupyter
Make sure we have jupyter notebook installed in your machine. If you 
are using Anaconda, jupyter comes pre-packaged and it's already installed. If you are not using Anaconda, you probably have to install jupyterlab or jupyter notebook. If you are want to install jupyterlab directly, without using Anaconda, you can open the terminal and run:

```{shell}
pip install jupyterlab
```

#### PyStata

```bash
pip install pystata
```

#### Stata Setup

+ a. Open the terminal and install stata_setup:

```bash
pip install stata_setup

pip install --upgrade --user stata_setup
```

+ b. Then, fix the stata set_up file by opening `stata_setup` file and change line `45` with:

```nano
config.init(edition)
```

+  c. Locate path to the folder containing Stata. If you use Windows, it is probably `C:\Program Files\Stata16\ado`. If you use Mac, it is `/Applications/Stata/ado`. If you use Unix, it is `/usr/local/stata16/ado`. In Stata type:

```stata
display c(sysdir_stata)
```

+ d. Open the `constants.py` file under `src`. Change these variables to match the edition and path to the folder containing Stata in your machine. 

```python
sys_dir = "/Applications/Stata/"
stat_edi = "mp"
```

#### Other packages

```{shell}
python -m pip install -U pip

python -m pip install -U matplotlib
```

#### Stata Jupyter Kernel

The Stata Jupyter Kernel enables using stata directly in jupyter notebooks.
To install in your local computer directly, open terminal and run:

```{shell}
pip install -U git+https://github.com/kylebarron/stata_kernel
python -m stata_kernel.install
```

To install using anaconda tools, it is important to specify -y when issuing install requests via conda as there is no way to accept the user requested y input to proceed with install. Then, run:

```conda
conda install -y -c conda-forge stata_kernel
```
Once the software is installed you need to install the jupyter kernel on your computer.

```bash
python -m stata_kernel.install
```

### 3.3. Launch Jupyter Notebook

Once installed, launch your notebook with the following commands:

> jupyter lab

```bash
jupyter-lab
```

> jupyter notebook
```bash
jupyter notebook
```

<a name="kick"></a>


## 4. Kick-off

There are two ways to run Stata code in jupyter notebook, if you want to use a Stata Kernell to run Stata code in Jupyter, then you must select the `Stata` kernell.

Execute the jupyter notebooks available at the following path `notebooks`:

+ [notebook-pystata.ipynb](https://github.com/rlmic/literate-economic-analysis/blob/main/notebooks/notebook-pystata.ipynb)

+ [notebook-stata-kernel.ipynb](https://github.com/rlmic/literate-economic-analysis/blob/main/notebooks/notebook-stata-kernel.ipynb)



<a name="misc"></a>

## 5. Miscellaneous

### 5.1. Quick Start

+ Command line install Anaconda on macOs. You can check how to install Anaconda in windows, following the instructions in [Anaconda](https://docs.anaconda.com/free/anaconda/install/).

Use this method if you prefer to use a terminal (highly recommended). Make sure you have preinstalled `xcode`, `brew` and `wget`.

    + Open terminal

    + Prerequirements

Make sure you have preinstalled `xcode`, `brew` and `wget`.

```{bash}
# install xcode
xcode-select --install
```

```{bash}
# install homebrew
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

```{bash}
# install brew
brew install wget
```

+  Download miniconda

```{bash}
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-x86_64.sh -O ~/miniconda.sh
```

```{bash}
bash ~/miniconda.sh -b -p $HOME/miniconda
```

+  Change paths

```{bash}
source <path to conda>/bin/activate
```

```{bash}
conda init zsh
```

+  Install necessary packages in conda enviroment.

```
pip install stata_setup
```

```{bash}
pip install pystata
```

+ Clone repository

```{bash}
git clone https://github.com/rlmic/literate-economic-analysis.git
```

+ Launch jupyter lab

```{bash}
jupyter lab
```

+ Change PYTHONPATH
```{bash}
export PYTHONPATH=$PWD
```

+ Jupyter notebook to HTML 

```{bash}
jupyter nbconvert --execute --to html notebook.ipynb
```


Click here to see an interactive example:


![Example](https://github.com/rlmic/literate-economic-analysis/blob/main/images/gifs/out.gif)



### 5.2 Key jupyter notebook shortcuts

+ `shift + enter` to run an active cell

+ `esc + L` - show line numbers

+ `esc + M` - format cell as Markdown cell

+ `esc + a` - insert cell above current cell

+ `esc + b` - insert cell below current cell

### 5.2 Other  useful resources

> Command line
+ [Introduction to command line](https://tutorial.djangogirls.org/en/intro_to_command_line/)

+ [Command line for beginners](https://learndjango.com/tutorials/terminal-command-line-beginners)

> Python

+ [Installing Python with Anaconda](https://quantecon.github.io/2021-workshop-rsit/resources/python-setup.html#resources-setup)

+ [Anaconda Prompt](https://conda.io/projects/conda/en/latest/user-guide/install/windows.html)

+ [Python for Windows](https://www.digitalocean.com/community/tutorials/install-python-windows-10)

+ [Python on Linux](https://docs.python-guide.org/starting/install3/linux/)

> Github
+ [Creating a new GitHub account](https://docs.github.com/en/get-started/signing-up-for-github/signing-up-for-a-new-github-account) 
+ [CarpentryCon 2022: Skill-up - Using GitHub for Collaboration in Open Source Communities](https://youtu.be/Vcckl-2dASM?t=5915)

> Computational notebooks
+ [Environmental Data Science book](https://edsbook.org/notebooks/gallery/ac327c3a-5264-40a2-8c6e-1e8d7c4b37ef/notebook.html)


> Jupyter

+ [Install Jupyter](https://jupyter.org/install)

+ [Jupyter notebook](https://jupyter.org/install)

> Stata and Jupyter

+ [RSIT Workshop 2021](https://quantecon.github.io/2021-workshop-rsit/week2/session7/stata-and-jupyter.html)

+ [stata_kernel](https://kylebarron.dev/stata_kernel/)

+ [Stata and R in a jupyter notebook](https://notebook.community/jhconning/Dev-II/notebooks/Stata_in_jupyter)

+ [Stata and Jupyter](https://medium.com/the-researchers-guide/how-to-use-stata-and-python-together-directly-from-jupyter-notebook-708fa25dab7a)

+ [PyStata](https://www.stata.com/python/pystata/install.html)



</div>



[^1]: This tutorial was launched as part of the [Research Transparency and Reproducibility Training (RT2) 2023](https://www.bitss.org/event-types/rt2-institute/), a confederence hosted at the University of California, Berkeley that aims to provide an overview of tools and practices for transparent and reproducible social science research.
