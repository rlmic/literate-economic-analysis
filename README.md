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