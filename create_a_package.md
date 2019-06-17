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

*Take-away 3* [Make tests for the functions](https://github.com/opengeophysics/2018-agu-oss-example-repo/blob/a8f279d9278d90c11027fba0a15340a37fed2c58/example-data-analysis.ipynb). Building tests for our code is important so that we know it gives the right results as we keep making modifications. The tests can also be automated and put on external servers (coming up later!) <br><br>
For function tests in python, we commonly use `assert`. General syntax is `assert np.all(<some-condition>)`. Here `np.all` will return a boolean array according to the condition we have set and `assert` will return `True` if all values in the array are `True`. `np.allclose` actually is better as it we can set a tolerance for match. Useful because floats are always approximate.

*Take-away 3:* Move the functions into a [seperate `.py` file](https://github.com/opengeophysics/2018-agu-oss-example-repo/blob/36265bf5af89977c792a9e2d343f035c07f8b3f3/data_analysis.py) or a module. Putting functions into scripts for library makes them easily reusable instead of copy/pasting code again and again.

*Take-away 4:* Put a doc-string at top for the module, and a doc-string for each function. 

### Part 2: Publishing the functions as a package



