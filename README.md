# First and Follow Set
This repository contains Python code to compute the First and Follow sets of a given grammar. The First and Follow sets are used in compiler construction to determine the possible terminals that can appear at the beginning and end of a non-terminal in a grammar.

# Requirements
The code in this repository requires Python 3.6 or higher to run.

# Usage
The code provides a Grammar class, which can be used to create a new grammar object by passing in the productions of the grammar as a dictionary. For example:

```
from grammar import Grammar

productions = {
    "S": ["aA", "bB"],
    "A": ["c", "d"],
    "B": ["c", "e"]
}
```
grammar = Grammar(productions)
Once you have created a grammar object, you can use its first and follow methods to compute the First and Follow sets of the grammar. For example:

makefile
Copy code
# Compute the First sets of the grammar
first_sets = grammar.first()

# Compute the Follow sets of the grammar
follow_sets = grammar.follow()
The first and follow methods return dictionaries that map non-terminals to their corresponding sets of terminals. For example, the first_sets dictionary might look like this:

```
{
    "S": ["a", "b"],
    "A": ["c", "d"],
    "B": ["c", "e"]
}

```
Testing
The repository also includes a test file test_grammar.py that contains test cases for the Grammar class. To run the tests, you can use the following command:

```
python test_grammar.py
```

# Contribution
Contributions are welcome! If you find a bug or have a feature request, please create an issue on the repository. If you would like to contribute code, please fork the repository and submit a pull request.
