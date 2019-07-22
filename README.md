# ERES V Github workshop

**Conveners:**
Ishan Mishra,
Ryan Petersburg,
Bastien Brugger


## Description

Coding makes up a significant part of a researcher’s time, yet scientists are known to have kept bad habits from early days of programming. The modern open-source community has developed tools and good practices for making software available and maintainable, useful for the reproducibility of studies required by scientific guidelines. This workshop will focus on GitHub, a code-hosting platform, to explain how version control systems work and can be used to improve the quality and quantity of programming among researchers. We will also go through other options offered by GitHub, such as creating your own website, and supplementary resources available within the open-source community.


## Agenda

| **9:00 - 10:15** | **Topic**|
|:----------------:|:---------------|
| 15 min | 1. Motivation for this workshop |
| 30 min | 2. How do Git & GitHub work: creating your account & first repo |
| 30 min | 3. Actual test project: fork repo, create new branch, edit files, pull request, merge |
| _10:15 - 10:45_ | _Break_ |
| **10:45 - 12:00** | **Topic** |
| 15 min | 4. Best practices for code accessibility and documentation |
| 30 min | 5. From a simple python script to a publishable package |
| 15 min | 6. Creating your website with GitHub Pages |
| 15 min | Discussion |



## Material

### Parts 1 & 2: motivation and functioning ([PDF](https://github.com/BastienBrugger/ERESV-github/blob/master/Part_1.pdf))

* [Merali (2010)](https://www.nature.com/news/2010/101013/full/467775a.html) *Error… why scientific programming does not compute*
* What is VCS? Git? GitHub? A small [handbook](https://guides.github.com/introduction/git-handbook/) to make things clear
* [GitHub Glossary](https://help.github.com/en/articles/github-glossary)
* Guide to [GitHub Flow](https://guides.github.com/introduction/flow/)
* Guide to [Create your first repo](https://guides.github.com/activities/hello-world/)
* List of [GUI clients](https://git-scm.com/downloads/guis/) options
* Installing Git as command line for [Linux](https://git-scm.com/download/linux), [MacOS](https://git-scm.com/download/mac) and [Windows](https://git-scm.com/download/win)


### Part 3: test project ([PDF](Part_2.pdf))

* Project [step-by-step](git-test-project.md)
* [Oh, shit, git!](http://ohshitgit.com) Where to go if a problem occurs
* Guide to [Forking a repo](https://guides.github.com/activities/forking/)


### Part 4: best practices for code accessibility and documentation

* Use and [properly format](https://chris.beams.io/posts/git-commit/) Git commit messages
* Github's [issue tracker](https://guides.github.com/features/issues/)
* [Beginner's Guide to Documentation](https://www.writethedocs.org/guide/writing/beginners-guide-to-docs/)
* [Documentation in Python](https://realpython.com/documenting-python-code/)
  * [Style guide for Python Code](https://www.python.org/dev/peps/pep-0008/) (PEP 8)
  * [Python Docstring Convention](https://www.python.org/dev/peps/pep-0257/) (PEP 257)
  * [Packaging your Python Project](https://the-hitchhikers-guide-to-packaging.readthedocs.io/en/latest/) - setup your python scripts as a python package and upload it to PyPi
* [Google's Open-Source Style Guide](https://github.com/google/styleguide)


### Part 5: From a simple python file/notebook to a publishable python package ([document](https://github.com/BastienBrugger/ERESV-github/blob/master/create_a_package.md))

Summary:

| Topic | Tools |
|:------|:------|
| Refactoring code to have 1) data downloadable through link (2) functions 3) tests for functions| Jupyter notebook, `assert` |
| How to setup a small Python library (though the example is in python, participants are encouraged to use their own research code in whichever language they prefer) | [Python packaging guide](https://packaging.python.org/tutorials/packaging-projects/#creating-setup-py)
| Use doc-strings for functions and modules| [Python Docstring Convention](https://www.python.org/dev/peps/pep-0257/) (PEP 257), other resources from Part 4|
|Overview of version control with git and setting up an online repository|resources from Parts 1-3|
| Discussion on choosing an open-source license| [Choose a license](https://choosealicense.com/), [OSI Licenses](https://opensource.org/licenses)|
| Including a Code of Conduct and Contributing Guidelines | [Contributor Covenant](https://www.contributor-covenant.org/), [Code of Conduct](https://help.github.com/en/articles/adding-a-code-of-conduct-to-your-project)  |
| How to write automated tests in Python | [Pytest](https://docs.pytest.org/en/latest/contents.html) |
| Setup continuous integration services to check that the code is tested on every update | [TravisCI](https://docs.travis-ci.com/user/languages/python/) |
| Write and publish documentation on ReadTheDocs, a free hosting service for open source software projects | [ReadTheDocs](http://readthedocs.org) |

### Part 6: website with GitHub Pages ([document](https://github.com/BastienBrugger/ERESV-github/blob/master/create-your-website.md))


#### Markup languages guides:

1. Basic markdown guides 
  - Guide to [GitHub Pages with Markdown](https://guides.github.com/features/pages/)
  - [Mastering Markdown](https://guides.github.com/features/mastering-markdown/)
  - Practice on an online Markdown editor (https://dillinger.io/). Jupyter notebooks have markdown cells as well. 
  - Markdown quick reference cheat sheets: https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet and https://en.support.wordpress.com/markdown-quick-reference/
2. Primers on HTML and CSS styling. 
  - HTML: https://www.w3schools.com/html/html_basic.asp
  - CSS: https://www.w3schools.com/html/html_css.asp
  - [A quick preview](http://wwwcodes.com/css-Tutorial/lab-images/input-css-output.png)


### Other interesting GitHub based resources for your research:

|Tool|Description|
|:------|:------|
|**[GitHub Guides](https://guides.github.com/)**|A set of guides to GitHub (check also their [videos](https://www.youtube.com/user/GitHubGuides/videos))|
|**[GitHub for Atom](https://github.atom.io/)**|A GitHub plugin for the Atom text editor, in case you don't want to install a complete Git GUI client|
|**[Start Bootstrap](https://startbootstrap.com/)**|A library of free open-source website themes and templates that you can download or directly view on GitHub|
|**[Zenodo](https://zenodo.org/), [Figshare](https://figshare.com/)**|For sharing large data files used in your research; version control; DOIs for data|
|**[CorTex](https://github.com/rodluger/corTeX)**|A living paper! The paper lives in a GitHub repository. Figures are generated by python scripts and maintained up to date by Travis-CI|
|**[Git Lfs](https://git-lfs.github.com/)**| Version control for large data files|

### Screencast of workshop on [Youtube](https://www.youtube.com/watch?v=HI-QK5PrCcY)
Have other resources to suggest? Feel free to [add an issue](https://github.com/BastienBrugger/ERESV-github/issues) to this repository! :)
