# Style conventions when it comes to Python files
## Differences with PEP 8
Although [PEP 8](https://peps.python.org/pep-0008/) is a generally accepted style guide for Python, [Athena's Chaos Drive Code](https://github.com/Athena-Chaos-Driven-Code) doesn't always follow this to the letter.
The following are exceptions to the "normal" PEP 8 style guide.
(PEP 8 is a guide, and is not supposed to be the end-all of how to write Python Code)

## Indentation
Functions that have multiple arguments that don't fit onto a single line, must be split into multiple different lines, where every argument is placed on a separate line.
```python
foo = long_function(
	a="a",
	b="b",
	...
)
```

## Maximum Line Length
The line length is set at 80 characters

## Strict Type annotations
Where possible, always annotate the types of variables, arguments, functions and outputs.

```python
def example_function(a:int, b:str="b") -> None
	return
```

## Naming Styles
CamelCase is only used for classes
UPPERCASE is used for static data
snake_case is used for everything else

```python
EXAMPLE:str = "example" # this piece of string is never to be edited by the script

class Foo:
	pass

def function_bar(a:Any, b:Any) -> None
	return

foo:Foo = Foo()

```

## Import rules
Imported packages are devided into three categories: 
- General Packages : Packages are either from the standerd library, or third party
- Athena Packages : Packages are written by Andreas, but aren't part of the current project
- Local Imports  : Packages and modules that are part of the current project

Imports are grouped together by module, and shouldn't be split up in different lines. 
When the amount of imported items exceeds the column count of 80 characters, the items are to be expected to be wrapped in round brackets and spread over multiple lines to not exceed the character column limit.
If different lines for each imported object is required, then there will only be one import statement with the different objects grouped together by round brackets.

```python
# Example of normal course of action
from foo import bar, egg, ...

# Example of too many items from a single import
from foo import (
	a, b, c, d, e, f, ...
)

# Example of imported item per line
from foo import (
	a,
	b,
	c,
	d,
	e,
	f,
	...
)
```