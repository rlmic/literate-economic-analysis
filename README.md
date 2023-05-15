<p align="left">
<img src="https://i0.wp.com/www.bitss.org/wp-content/uploads/2019/03/CEGA-logo-RGB-300-dpi-colour.png?ssl=1" data-canonical-src="https://www.bitss.org" width="280" height="120" />
</p>


<h1 align="center">

<b>Literate Economic Data Analysis </b>

</h1>

<h2 align="center">

<b>Computation Notebooks</b>

</h2>

<p align="center">
<img src="https://cega.berkeley.edu/wp-content/uploads/2018/10/sidebar_Final-logo_vertical-01_2_3_1.png" data-canonical-src="https://www.bitss.org" width="200" height="230" />
</p>

<p align="center">
Daniela Pinto Veizaga
</p>
<p align="center">
University of California, Berkeley
</p>
<p align="center">
CEGA
</p>

## 0. :wave: Introduction
<p align="justify">
Computation notebooks have become a successful mechanism for prototyping and writing examples to showcase a piece of software, sharing data analysis and documenting research workflows. The Literate Economic Data Analysis (LEDA) workshop is a hands-on tutorial[^1] through which we will learn how notebooks can complement the science and methodological development of social science research.
</p>

<p align="center" width="100%">
    <img src="https://edsbook.org/_images/notebook-cycle.jpg" width="80%" height="410" />
</p>

<p align="center">
Source: The Turing Way project. Illustration by Scriberia as part of The Turing Way book dash in November 2022. Zenodo. http://doi.org/10.5281/zenodo.7587336
</p>

### Who is this workshop for?
<p align="justify">
This workshop is designed for those who want to take their data analysis skills and expertise in Stata and potentiate them with computation notebooks. Jupyter notebook is one such form of interactive computing environment that offers multilingual programming language support to create dynamic and static documents, books, presentations, blogs, and resources. 
</p>

<p align="justify">
The workshop will introduce you to create static documents with Jupyter notebooks, add interactivity to them and integrate them with your regular workflow in Stata, translating code, widgets, narrative text, equations, and graphical objects into one working, collaborative, interactive and reproducible document.
</p>


### What we will cover?
<p align="justify">
The curriculum lays out the importance of reproducibility in the context of economic data analysis, and providing an overview of the common concepts, tools and resources. We assume atendees are familiar to version control, testing, and reproducible computational environments. We build on these core concepts, to boost our data analysis skills integrating Jupyter Notebooks, Python and Stata.
</p>
The curriculum is as follows:

1. [ Background. ](#back)
2. [ Prerequirements. ](#preq)
3. [ Setup Instructions. ](#setup)
4. [ Kick-off. ](#kick)


<a name="back"></a>
## 1. Background

<p align="justify">
The name of this workshop is inspired in Donald Knuth's conceptual use of literate programming, defined as a script, notebook, or computational document that contains an explanation of a program's logic in a natural language, with snippets of macros and source code, which can be compiled and rerun. An executable paper!
</p>
<p align="justify">
As economists we draw on a handful of statistical softwares, such as Stata, R, and Python, to implement our econometric analysis. Regarless of our software preferance, it is of our best interest to ensure our analysis is reproducible adn executable by anybody. The number one cause of irreproducible research is that authors produce their analysis out of order and without proper documentation. 
</p>
<p align="justify">
Jupyter notebooks are heavily used in data science, because of it's  The jupyter name comes from 3 programming languages: Julia, Python, and R. You can use one programming language per document, and it is done through choosing a kernel (e.g. Python, R, Go, and more -- get the full list of kernels from the wiki).
</p>


Jupyter notebooks can be comprised mainly of two types of cells (though more can be added with plugins).

Markdown Cells (for narratives): when run, a markdown cell will display markdown or HTML that you write (that means all sort of rich content, including images). Essential markdown summary: https://daringfireball.net/projects/markdown/syntax
Code Cells (for data cleaning, analysis, visualization, etc.): executable code in a variety of languages, dictated by the kernel (default is Python, but more can be added).
Some key jupyter notebook shortcuts to keep in mind while you work:

Use shift + enter to run an active cell

Use esc in highlighted cell to toggle command options:

esc + L - show line numbers

esc + M - format cell as Markdown cell

esc + a - insert cell above current cell

esc + b - insert cell below current cell

Check all current variables: run %whos from a code cell

RMarkdown
RMarkdown is another popular literate programming tool and can be considered an extension of Markdown. Like all literate programming tools, it  mixes documentation & code, and not just R code either! You can insert code snippets from other languages (SQL, bash, Python, etc.) into ONE DOCUMENT! Incorporating results directly into your documents is an important step in reproducible research. Any changes that occur in either your data set or the analysis are automatically updated in your document the next time the document is created.

Typically, RMarkdown files are edited from within RStudio. The R for Data Science book contains a great chapter on RMarkdown for more information: https://r4ds.had.co.nz/r-markdown.html.

<a name="preq"></a>
## 2. Prerequirements

To adequately follow through the workshop, you must have:

+ Python and Stata installed in your machine,
+ Some experience working with the command line,
+ A GitHub account.

If you do not meet the minimum prerequirements, the workshop will prove a bit more difficult than expected. Please take sometime before our workshop to fulfill these prerequirements and be ready to go. During our workshop we might take a few minutes ensure everyone is ready to go.

### 2.1 Software installation

### a. Command Line



### b. Python

OS X

Python is probably already installed on your system. To check if it’s installed, go to Applications > Utilities and click on Terminal.

On

Find out which version of Python is installed by issuing the command python --version:
Install Python with Homebrew

Homebrew is a package installer.


Python installed in our systems

Install Python with Homebrew

Homebrew is a package installer.

First, install Homebrew.

```bash
$ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```

Then, install brew to Path:

```bash
$export PATH="/usr/local/opt/python/libexec/bin:$PATH"
```

Next, install Python.

```bash
$brew install python
```

Ubuntu Linux machines.

To see which version of Python 3 you have installed, open a command prompt and run

$ python3 --version
If you are using Ubuntu 16.10 or newer, then you can easily install Python 3.6 with the following commands:

$ sudo apt-get update
$ sudo apt-get install python3.6
If you’re using another version of Ubuntu (e.g. the latest LTS release) or you want to use a more current Python, we recommend using the deadsnakes PPA to install Python 3.8:

$ sudo apt-get install software-properties-common
$ sudo add-apt-repository ppa:deadsnakes/ppa
$ sudo apt-get update
$ sudo apt-get install python3.8
If you are using other Linux distribution, chances are you already have Python 3 pre-installed as well. If not, use your distribution’s package manager. For example on Fedora, you would use dnf:

$ sudo dnf install python3
Note that if the version of the python3 package is not recent enough for you, there may be ways of installing more recent versions as well, depending on you distribution. For example installing the python3.9 package on Fedora 32 to get Python 3.9. If you are a Fedora user, you might want to read about multiple Python versions available in Fedora.


### c. Github

GitHub is a code hosting platform for version control and collaboration, widely use to store and share code, track changes, and collaborate on projects with others. To start using GitHub, you need to create an account. You can do this by clicking [here](https://github.com) and signing up for a free account.

Additional resources:

+ Creating a [new GitHub account](https://docs.github.com/en/get-started/signing-up-for-github/signing-up-for-a-new-github-account) 
+ Learning more about how GitHub can support collaborative documentation-writing and knowledge sharing: [CarpentryCon 2022: Skill-up - Using GitHub for Collaboration in Open Source Communities](https://youtu.be/Vcckl-2dASM?t=5915).

### d. Stata

Adquire your Stata license and install it your computer. [Stata's website](https://www.stata.com/install-guide/) is comprehensive in terms of the steps needed to install Stata.



<a name="setup"></a>
## 3. Setup Instructions

### 3.1. Clone repository

To start working on your code locally or remotely, you need to clone the repository. To do this, click on the green “Code” button and copy the URL. Then, open up your terminal (or command prompt on Windows) and navigate to the directory where you want to store your code. In the command line type:

```{bash}
git clone https://github.com/rlmic/literate-economic-analysis.git
```

### 3.2. Install required packages
First, make sure we have Jupyter Notebook installed in your machine. If not installed, [please install](https://jupyter.org/install).

```{shell}
pip install jupyterlab
```
##### PyStata

```bash
pip install pystata
```

```bash
pip install stata_setup
```

open stata_setup and change line 45 with "config.init(edition)"

In Stata, enter the following command to locate the folder containing Stata 17 : display c(sysdir_stata)

pip install --upgrade --user stata_setup


If you use Windows, it is probably C:\Program Files\Stata16\ado, but it might be someplace else. If you use Mac, it is /Applications/Stata/ado. That is, it is the ado folder in the official Stata folder. If you use Unix, it is /usr/local/stata16/ado.

First of all, you need to install the Anaconda Prompt (conda). Tou have to follow the instructions on the conda website: https://conda.io/projects/conda/en/latest/user-guide/install/windows.html.

Then, you have to install the jupyter notebook. The instructions are available on their website: https://jupyter.org/install.

In a third step, you have to install PyStata: https://www.stata.com/python/pystata/install.html.

In Stata, enter the following command to locate the folder containing Stata 17 : display c(sysdir_stata)

The software is in this folder 'C:\Program Files\Stata17/' in my case and I use the standard edition.

In conda, install PyStata : pip install --upgrade --user stata_setup

Lastly, you have to install the matplotlib library for an illustration with a 3D graph: https://matplotlib.org/stable/users/installing.html

In conda, you can type:

python -m pip install -U pip

python -m pip install -U matplotlib

Now, you are ready to launch Stata from the Jupyter Notebook.

Lastly, you have to install the matplotlib library for an illustration with a 3D graph: https://matplotlib.org/stable/users/installing.html

In conda, you can type:

python -m pip install -U pip

python -m pip install -U matplotlib

Now, you are ready to launch Stata from the Jupyter Notebook.


##### Stata Jupyter Kernel¶

pip3 install -U git+https://github.com/kylebarron/stata_kernel
python3 -m stata_kernel.install
There is also excellent documentation available.
The Stata Jupyter Kernel enables using stata directly in jupyter notebooks.

It is effectively an alternative interface to use stata if you like jupyter as an interface.

This can be useful if you want to write notebooks that are integrated with stata code.

It supports a wide range of interaction with stata

To install using anaconda tools you can use the following commands in a jupyter notebook:

It is important to specify -y when issuing install requests via conda as there is no way to accept the user requested y input to proceed with install. pip doesn’t have this issue as it doesn’t request user input.
!conda install -y -c conda-forge stata_kernel
Copy to clipboard
once the software is installed you need to install the jupyter kernel on your computer

!python -m stata_kernel.install
Copy to clipboard
Warning
[macOS] When I ran the kernel install step I got the following error:

Cannot import kernel
Installing Jupyter kernel spec
WARNING: Could not find Stata path.
Refer to the documentation to see how to set it manually:

https://kylebarron.dev/stata_kernel/using_stata_kernel/configuration
Copy to clipboard
and had to manually set the stata path in the .stata_kernel.conf file located in your home directory to the following:

# Path to stata executable. If you type this in your terminal, it should
# start the Stata console
stata_path = /Applications/Stata/StataIC.app/Contents/MacOS/StataIC

# **macOS only**
# The manner in which the kernel connects to Stata. Either 'console' or
# 'automation'. 'console' is the default because it allows multiple
# independent sessions of Stata at the same time.
execution_mode = automation
Copy to clipboard
Unfortunately StataIC is limited on mac os so I had to use automation instead of console as per this issue in the docs However this does enable the use of browse
If you start jupyter notebook you should now see a stata kernel option. If selected a jupyter notebook will open with a connection to stata. You can verify this on the top-right of the notebook

References:
https://kylebarron.dev/stata_kernel/
https://quantecon.github.io/2021-workshop-rsit/week2/session7/stata-and-jupyter.html

https://notebook.community/jhconning/Dev-II/notebooks/Stata_in_jupyter
https://medium.com/the-researchers-guide/how-to-use-stata-and-python-together-directly-from-jupyter-notebook-708fa25dab7a


### 3.3. Launch Jupyter Notebook

Once installed, launch your notebook with the following command:

```bash
jupyter-lab
```

<a name="kick"></a>

## 4. Kick-off

Execute the jupyter notebooks available at the following path `notebooks`:

+ [notebook-pystata.ipynb](https://github.com/rlmic/literate-economic-analysis/blob/main/notebooks/notebook-pystata.ipynb)

+ [notebook-stata-kernel.ipynb](https://github.com/rlmic/literate-economic-analysis/blob/main/notebooks/notebook-stata-kernel.ipynb)


## Other resources

+ [Environmental Data Science book](https://edsbook.org/notebooks/gallery/ac327c3a-5264-40a2-8c6e-1e8d7c4b37ef/notebook.html)


[^1]: This tutorial was launched as part of the [Research Transparency and Reproducibility Training (RT2) 2023](https://www.bitss.org/event-types/rt2-institute/), a confederence hosted at the University of California, Berkeley that aims to provide an overview of tools and practices for transparent and reproducible social science research.