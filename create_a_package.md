## From a simple python file/notebook to a publishable python package

### Massive credits: [AGU 2018 Open Source Software workshop](https://github.com/agu-ossi/2018-agu-oss) 

### Motivation

1. Make the code easily reusable
2. Make the code robust
3. Make the code version controlled
4. Make the code easily collaborative
5. Make the code well documented


### Starting point: [simple script/jupyter notebook](https://nbviewer.jupyter.org/github/opengeophysics/2018-agu-oss/blob/master/example-data-analysis.ipynb) that downloads data and does some analysis on it

### Part 1: Refactoring the notebook

*Take-away 1:* Avoid using locally stored data. Download data directly from URL if possible. This makes the code more easily reusable.

*Take-away 2:* [Refactor code to use functions](https://github.com/opengeophysics/2018-agu-oss-example-repo/blob/a8f279d9278d90c11027fba0a15340a37fed2c58/example-data-analysis.ipynb) to make it more reusable and testable.

*Take-away 3* [Make tests for the functions](https://github.com/opengeophysics/2018-agu-oss-example-repo/blob/a8f279d9278d90c11027fba0a15340a37fed2c58/example-data-analysis.ipynb). 
- Building tests for our code is important so that we know it gives the right results as we keep making modifications. 
- The tests can also be automated and put on external servers (coming up later!) 
For function tests in python, we commonly use `assert`. General syntax is `assert np.all(<some-condition>)`. Here `np.all` will return a boolean array according to the condition we have set and `assert` will return `True` if all values in the array are `True`.
- `np.allclose` actually is better as it we can set a tolerance for match. Useful because floats are always approximate.

*Take-away 4:* Move the functions into a [seperate `.py` file](https://github.com/opengeophysics/2018-agu-oss-example-repo/blob/36265bf5af89977c792a9e2d343f035c07f8b3f3/data_analysis.py) or a module. Putting functions into scripts for library makes them easily reusable instead of copy/pasting code again and again.

*Take-away 5:* Put a doc-string at top for the module, and a doc-string for each function. A great reference is python's popular and well documented libraries and functions, for example [numpy.mean](https://github.com/numpy/numpy/blob/v1.16.1/numpy/core/fromnumeric.py#L3014-L3118)

### Part 2: Publishing the functions as a package

This is a good point to put our code on [GitHub](https://guides.github.com/activities/hello-world/). We create a new repository


*Take-away 6*: Always a good idea to initialize with [a README file](https://github.com/opengeophysics/2018-agu-oss-example-repo/blob/89bc4680339ca98c1800706b1e8cae14dffc29bf/README.md).

  -A brief explanation of what the code does should suffice. 
  -Later we can add some info about installing and links to documentation, etc.

*Take-away 7*: Initialize your repository with a license file and a `.gitignore` file.

  - For `gitignore`, selecting Python would setup the repository so that the auxiliary python files are not tracked. For example, temporary files that are created by Jupyter notebooks (Jupyter notebooks have their own version of version control file stored in a folder called .ipynb checkpoints) ([official list of .gitignore files](https://github.com/github/gitignore))
  - There are [different types of licenses](https://choosealicense.com/) available depending on we want people to use our code. Python mostly has MIT and BSD license which means it be used by both academics and industry and is completely open source.
  - Having no license means its your copyright and no one else is allowed to use it or adapt it, which prevents easy collaboration; others can spot bugs and make the code more usable. *People usually think otherwise and it creates a confusing and potentially tough situation*.
  - Licenses take away liability as well.
  - Don't write your own license!

*Take-away 8*: Create a [code of conduct file.](https://github.com/opengeophysics/2018-agu-oss-example-repo/blob/876638335a4d2b5f0ad5d0fcb5458eda06d8842a/CODE_OF_CONDUCT.md) and a [contributing guide](https://github.com/opengeophysics/2018-agu-oss-example-repo/blob/master/CONTRIBUTING.md)
 
  
  - After initializing the repository, we *clone* the repository to our local machine, *add* the files local files to be tracked, *commit* them and *push* them to the repository. 
  
  ### PAUSE! 
  
  [This is what the repository looks like in the present stage.](https://github.com/opengeophysics/2018-agu-oss-example-repo/tree/fef35145fe2e52cee0033783778eb7674ccb525e) 
  
 Next we want to officially make a package from our `.py file` that contains the function
 - We move our `data_analysis.py` file to a folder called <whatever-name-we-want>. We also add `__init__.py` in the folder, that basically defines the folder as being a package. 
 - We create a [`setup.py`](https://github.com/opengeophysics/2018-agu-oss-example-repo/blob/876638335a4d2b5f0ad5d0fcb5458eda06d8842a/setup.py) file in the home directory for installing our package.  
 - The `setup.py` files uses a package called `setuptools`, which is a set of functions and conventions that define how packages are built in python
  
So, *Take-away 9* is that we need an `__init__.py` to let python know that a folder is a package, and a `setup.py` file in the home directory for installing the package.

*Take-away-10*: Add installation instructions:
- To install the package: `pip install -e .`
  - `-e` means editable installation (creates a link to this folder instead of copying the contents as they stand right now to python's root folder; the package stays alive and future edits are automatically incorporated when you import the package.
  - `.` indicates current directory
  
 [This is what the repository looks like in the present stage.](https://github.com/opengeophysics/2018-agu-oss-example-repo/tree/1491609fda07b97f99197440ec8f482adfc2f115)
 
 
 *Take-away-11*: Create a separate [test module](https://github.com/opengeophysics/2018-agu-oss-example-repo/blob/eacb151a663055915bb8012956bbd3070237391e/data_analysis/test_data_analysis.py)
 - running `pytest` in your package's home directory looks for all the files starting with `test_` and runs the test. In your local machine run `pytest -v` or `python -m pytest -v`
 - The testing can be automated by using external services known as Continuous Integration. A popular one is [Travis-CI](https://docs.travis-ci.com/user/languages/python/).
 - Travis-CI links to your GitHub repository, and runs the set of commands you specify in its [configuration file](https://github.com/opengeophysics/2018-agu-oss-example-repo/blob/96a97d7e36a18c5fb7ebe90468da828da3400cfb/.travis.yml) whenever it detects a change. 
 - Tests can be run for different versions of python, different os, etc. Make the code more robust.
 
 *Take-away-12*: Add a documentation folder (`docs/`) using [sphinx](https://docs.readthedocs.io/en/stable/intro/getting-started-with-sphinx.html#quick-start) and host it online using [ReadTheDocs](https://readthedocs.org/)
 
 - Popular option is Sphinx/ReadTheDocs
 - Sphinx is a python tool used to create beautiful Python documentation. All python language documentation is usually in Sphinx.
 - [Easy to follow steps]((https://pythonhosted.org/an_example_pypi_project/sphinx.html)) to create a basic documentation
 - Add project to ReadTheDocs to build a website from your repository. 
 
 ### Final verison of the repository: https://github.com/ishan-mishra/2019-eres-v-example
 
 
 
 


 
 
 
 
 
  




