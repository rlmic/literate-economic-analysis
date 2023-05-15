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

## :wave: Introduction

*Computation notebooks* have become a successful mechanism for prototyping and writing examples to showcase a piece of software, sharing data analysis and documenting research workflows. The Literate Economic Data Analysis (LEDA) workshop is a hands-on tutorial[^1] through which we will learn how notebooks can complement the science and methodological development of social science research.


<p align="center" width="100%">
    <img src="https://edsbook.org/_images/notebook-cycle.jpg" width="80%" height="410" />
</p>

<p align="center">
Source: The Turing Way project. Illustration by Scriberia as part of The Turing Way book dash in November 2022. Zenodo. http://doi.org/10.5281/zenodo.7587336
</p>

### Who is this workshop for?

This workshop is designed for those who want to take their data analysis skills and expertise in Stata and potentiate them with computation notebooks. Jupyter notebook is one such form of interactive computing environment that offers multilingual programming language support to create dynamic and static documents, books, presentations, blogs, and resources.

The workshop will introduce you to create static documents with Jupyter notebooks, add interactivity to them and integrate them with your regular workflow in Stata, translating code, widgets, narrative text, equations, and graphical objects into one **working, collaborative, interactive and reproducible document.**


### What will be cover in this guide?

Our number one priority at DSSG is to train fellows to do responsible data science/ML/AI for social good work. This curriculum includes many things you'd find in a data science course or bootcamp, but with an emphasis on solving problems with social impact, integrating data science with the social sciences, understanding and discussing ethical implications of the work, as well as privacy, and confidentiality issues.

We have spent many (sort of) early mornings waxing existential over Dunkin' Donuts while trying to define what makes a "data scientist for social good," that enigmatic breed combining one part data scientist, one part helper, one part educator, and one part bleeding heart idealist. We've come to a rough working definition in the form of the skills and knowledge one would need, which we categorize as follows:

Programming, because you'll need to tell your computer what to do, usually by writing code.
Computer science, because you'll need to understand how your data is - and should be - structured, as well as the algorithms you use to analyze it.
Math and stats, because everything else in life is just applied math, and numerical results are meaningless without some measure of uncertainty.
Machine learning, because you'll want to build predictive or descriptive models that can learn, evolve, and improve over time.
Social science, because you'll need to know how to design experiments to validate your models in the field, and to understand when correlation can plausibly suggest causation, and sometimes even do causal inference.
Problem and Project Scoping, because you'll need to be able to go from a vague and fuzzy project description to a problem you can solve, understand the goals of the project, the interventions you are informing, the data you have and need, and the analysis that needs to be done.
Project management, to make progress as a team, to work effectively with your project partner, and work with a team to make that useful solution actually happen.
Privacy and security, because data is people and needs to be kept secure and confidential.
Ethics, fairness, bias, and transparency, because your work has the potential to be misused or have a negative impact on people's lives, so you have to consider the biases in your data and analyses, the ethical and fairness implications, and how to make your work interpretable and transparent to the users and to the people impacted by it.
Communications, because you'll need to be able to tell the story of why what you're doing matters and the methods you're using to a broad audience.
Social issues, because you're doing this work to help people, and you don't live or work in a vacuum, so you need to understand the context and history surrounding the people, places and issues you want to impact.
All material is licensed under CC-BY 4.0 License: CC BY 4.0

Table of Contents

## Background
The name of this workshop is inspired in Donald Knuth's conceptual use of *literate programming*, defined as a script, notebook, or computational document that contains an explanation of a program's logic in a natural language, interspersed with snippets of macros and source code, which can be compiled and rerun. An executable paper!

As economists we draw on a handful of statistical softwares, such as Stata, R, and Python, to implement our econometric analysis. Regarless of our software preferance, it is of our best interest to matter which literate programming tool you use, only run the cells from top to bottom – ONLY. The number 1 cause of irreproducible jupyter notebooks is that the original authors run the cells out of order, which can't be reproduced without documentation about which cells in which order. So run your literate programming notebooks from top to bottom only.


reproducibility in the context of this handbook, laying out its importance for science and scientists, and providing an overview of the common concepts, tools and resources. The first few chapters were on version control, testing, and reproducible computational environments. Since the start of this project in 2019, many additional chapters have been written, edited, reviewed, read and promoted by over 300 contributors.
Jupyter Notebooks
Jupyter Notebook is an interactive computing environment that enables users to author notebook documents that include code, interactive widgets, plots, narrative text, equations, images and even videos! Jupyter notebooks are heavily used in data science, and it would behoove you to get comfortable with the tool. The jupyter name comes from 3 programming languages: Julia, Python, and R. You can use one programming language per document, and it is done through choosing a kernel (e.g. Python, R, Go, and more -- get the full list of kernels from the wiki).

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


## Quickstart

### Prerequirements

To adequately follow through the Workshop, you must have:

+ Python and Stata installed in your machine,
+ Some experience working with the command line,
+ A GitHub account.

If you do not meet the minimum prerequirements, the Worshop will prove a bit more difficult than expected. Please take sometime before our Workshop to fulfill these prerequirements and be ready to go. During our workshop we might take 10 minutes at most to ensure everyone is ready to go. However, to help you get up to speed with the prerequirements, please read the instructions and links provided.

#### Software installation

##### Python
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

```{bash}
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```

Then, install brew to Path:

```{bash}
$ export PATH="/usr/local/opt/python/libexec/bin:$PATH"
```

Next, install Python.

```{bash}
brew install python
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

##### Stata

Please adquire your Stata license and follow the instructions provided in [Stata's website](https://www.stata.com/install-guide/) to kickoff running code in Stata.

#### Command Line

#### Github

GitHub is a code hosting platform for version control and collaboration, widely use to store and share code, track changes, and collaborate on projects with others. To start using GitHub, you need to create an account. You can do this by going to [GitHub](https://github.com) and sign up for a free account.

Additional resources:

+ Creating a [new GitHub account](https://docs.github.com/en/get-started/signing-up-for-github/signing-up-for-a-new-github-account) 
+ Learning more about how GitHub can support collaborative documentation-writing and knowledge sharing: [CarpentryCon 2022: Skill-up - Using GitHub for Collaboration in Open Source Communities](https://youtu.be/Vcckl-2dASM?t=5915).


###  Setup Instructions

Now, we are ready to go.

#### 1. Fork/Clone repository

Clone the repository: To start working on your code locally or remotely, you need to clone the repository. To do this, click on the green “Code” button and copy the URL. Then open up your terminal (or command prompt on Windows) and navigate to the directory where you want to store your code. Type “git clone [repository URL]” to clone the repository.

#### 2. Set up virtual enviroment

1. Install virtualenv in your machine. If your machine has a linux-based operating system, run:

```
pip install virtualenv
```

Else, 

```
sudo apt-get install python-pip
```

2. Create a Virtual Python Environment

Locate yourself on your project directory and run virtualenv to create the new virtual environment.

```
cd literate-economic-analysis
virtualenv econ-repr
```

3. Activate the Environment

Now that we have a virtual environment, we need to activate it.

```
source econ-repr/bin/activate
```

After you activate the environment, your command prompt will be modified to reflect the change.

4. Add Libraries and Create a requirements.txt File

After you activate the virtual environment, you can add packages to it using pip. You can also create a description of your dependencies using pip.

The following command creates a file called requirements.txt that enumerates the installed packages.

```
pip freeze > requirements.txt
```

This file can then be used by collaborators to update virtual environments using the following command.

```
pip install -r requirements.txt

```

Deactivate the Environment. To return to normal system settings, use the deactivate command.

```
deactivate
```

#### Launch Jupyter Notebook

First, make sure we have Jupyter Notebook installed in your machine. If not installed, [please install](https://jupyter.org/install).

```
pip install jupyterlab
```

Add the virtualenv you've cretead in the previous step as a jupyter kernel.

```
ipython kernel install --name econ-repr --user
```

Once installed, launch JupyterLab with:

```
jupyter-lab

```


#### Quick-off

##### PyStata

```
pip install pystata
```

```
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
There is also excellent documentation available.
The Stata Jupyter Kernel enables using stata directly in jupyter notebooks.

It is effectively an alternative interface to use stata if you like jupyter as an interface.

This can be useful if you want to write notebooks that are integrated with stata code.

It supports a wide range of interaction with stata

To install using anaconda tools you can use the following commands in a jupyter notebook:

Tip
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

## Contact Information

Daniela Pinto Veizaga


[^1]: This tutorial was launched as part of the [Research Transparency and Reproducibility Training (RT2) 2023](https://www.bitss.org/event-types/rt2-institute/), a confederence hosted at the University of California, Berkeley that aims to provide an overview of tools and practices for transparent and reproducible social science research.