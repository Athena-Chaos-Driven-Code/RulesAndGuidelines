# Differences with PEP 8
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