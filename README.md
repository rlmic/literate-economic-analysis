# LITERATE ECONOMIC DATA ANALYSIS

The name of this workshop is inspired in Donald Knuth's conceptual use of *literate programming*, defined as a script, notebook, or computational document that contains an explanation of a program's logic in a natural language, interspersed with snippets of macros and source code, which can be compiled and rerun. An executable paper!

As economic analyst/researchers our main weapon/programming tool to produce these analysis are primarily Stata and R, though some of us may be equally familiar with other programming tools such as Julia, Python, C, and the list goes on. Regarless of our preferred tool, matter which literate programming tool you use, only run the cells from top to bottom – ONLY. The number 1 cause of irreproducible jupyter notebooks is that the original authors run the cells out of order, which can't be reproduced without documentation about which cells in which order. So run your literate programming notebooks from top to bottom only.

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

If you do not meet the minimum prerequirements, the Worshop will prove a bit more difficult than expected. Please take sometime before our Workshop to fulfill these prerequirements and be ready to go. During our workshop we might take 10 minutes at most to ensure everyone is ready to go. However, to To help you get up to speed with the prerequirements, please read the instructions and links provided in the following links:



#### Github

GitHub is a code hosting platform for version control and collaboration, widely use to work together on projects from anywhere.


If you do not have a github account, please make sure to follow [these](https://docs.github.com/en/get-started/signing-up-for-github/signing-up-for-a-new-github-account) instructions to create a new github account. 


##### OS X


Python is probably already installed on your system. To check if it’s installed, go to Applications > Utilities and click on Terminal.

On

Find out which version of Python is installed by issuing the command python --version:
Install Python with Homebrew

Homebrew is a package installer.


* Python installed in our systems

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

##### Ubuntu Linux machines.

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

### Setup Instructions

Now, we are ready to go.

#### Fork/Clone repository

#### Set up virtual enviroment

#### Quick-off
