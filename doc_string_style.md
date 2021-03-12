Documentation
- Documentation is used to make your code easier to understand and use. 
- Functions are especially readable because they often use documentation strings, or docstrings. 
- Docstrings are a type of comment used to explain the purpose of a function, and how it should be used. 
- Here's a function for population density with a docstring.

```py
def population_density(population, land_area):
    """Calculate the population density of an area. """
    return population / land_area
```

- Docstrings are surrounded by triple quotes. 
- The first line of the docstring is a brief explanation of the function's purpose. 
- If you feel that this is sufficient documentation you can end the docstring at this point; 
- single line docstrings are perfectly acceptable, as in the example above.
```py
def population_density(population, land_area):
    """Calculate the population density of an area.

    INPUT:
    population: int. The population of that area
    land_area: int or float. This function is unit-agnostic, if you pass in values in terms
    of square km or square miles the function will return a density in those units.

    OUTPUT: 
    population_density: population / land_area. The population density of a particular area.
    """
    return population / land_area
```

- If you think that a longer description would be appropriate for the function, 
- you can add more information after the one-line summary. 
- In the example above, you can see that we wrote an explanation of the function's arguments, 
- stating the purpose and types of each one. 
- It's also common to provide some description of the function's output.

- Every piece of the docstring is optional, however, docstrings are a part of good coding practice. 
- You can read more about docstring conventions here.

- Python docstrings can be written following several formats as the other posts showed. 
- However the default Sphinx docstring format was not mentioned and is based on reStructuredText (reST). 
- You can get some information about the main formats in this blog post.
Note that the reST is recommended by the PEP 287
There follows the main used formats for docstrings.
- Epytext
Historically a javadoc like style was prevalent, so it was taken as a base for Epydoc (with the called Epytext format) to generate documentation.
Example:
"""
This is a javadoc style.

@param param1: this is a first param
@param param2: this is a second param
@return: this is a description of what is returned
@raise keyError: raises an exception
"""
- reST
Nowadays, the probably more prevalent format is the reStructuredText (reST) format that is used by Sphinx to generate documentation. Note: it is used by default in JetBrains PyCharm (type triple quotes after defining a method and hit enter). It is also used by default as output format in Pyment.
Example:
"""
This is a reST style.

:param param1: this is a first param
:param param2: this is a second param
:returns: this is a description of what is returned
:raises keyError: raises an exception
"""
- Google
Google has their own format that is often used. It also can be interpreted by Sphinx (ie. using Napoleon plugin).
Example:
"""
This is an example of Google style.

Args:
    param1: This is the first param.
    param2: This is a second param.

Returns:
    This is a description of what is returned.

Raises:
    KeyError: Raises an exception.
"""
Even more examples
- Numpydoc
Note that Numpy recommend to follow their own numpydoc based on Google format and usable by Sphinx.
"""
My numpydoc description of a kind
of very exhautive numpydoc format docstring.

Parameters
----------
first : array_like
    the 1st param name `first`
second :
    the 2nd param
third : {'value', 'other'}, optional
    the 3rd param, by default 'value'

Returns
-------
string
    a value in a string

Raises
------
KeyError
    when a key error
OtherError
    when an other error
"""

