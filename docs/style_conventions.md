# Style Conventions
## Packages and Projects
### Name
Package name is written down in **CamelCase** and consists out of two sections: `Athena` and and abstract name for the package's feature

Examples:
- `AthenaLib`   : Collection of boilerplate code
- `AthenaColor` : Console coloring

### Version
Version strings of packages will follow [Semantic Versioning 2.0.0](https://semver.org/spec/v2.0.0.html) guideline of: `Major.Minor.Patch`
- Major : Changes to the API, that are incompatible with previous states of the code 
- Minor : Additions of functionality, that don't cause compatibility issues.
- Patch : Bug Fixes

### Files and Folders
files and folders within a package are to named with the **snake_case** convention
- This rule does not apply to the folder which is the root of a Package, which must be in **CamelCase** convention

A data file is supposed to be data that is grouped together by subject

Functions are to be grouped in a file by subject.

Objects should always be placed in their own file, some exceptions to this rule is allowed:
- A small support class, that is only used within the main class of the file
- solving circular import errors

Subfolders should only contain files that are grouped by subject.
- Example: Various Classes that define GUI views are grouped together in the `views` subfolder of `objects`.

General project setup:
```
├📁res
│   ├📁images
│   ├📁data
│
├📁docs
│
├📁src (Marked in PyCharm as the Source root)
│   ├📁Athena<Package>
│		├📁data (Static data like commonly used strings, enum, etc...)
│		├📁functions (Stand alone functions, decorators, and generators)
│		├📁objects (Classes)
│		├📄__init__.py (root imports)
│
├📁tests (collection of tests, different sub folders mark different subjects)
│
├📄.gitignore
├📄readme.md
├📄setup.py	

```

---
## File structure
Generally speaking, a file consists out of three sections:
- **Package Imports** :
	- General Packages : Imports from the standard library or 3rd party packages. Usually has the `from __future__ import annotations` at the top, even though the Python foundation doesn't really know how to implement the feature in full for the future.
	- Athena Packages : Package imports from withing [Athena's Chaos Drive Code](https://github.com/Athena-Chaos-Driven-Code)
	- Local Imports : Imports from the local project itself
- **Support Code** : A section that isn't always present in easy file, as it contains code that the main code relies on, like a regularly occurring string value, or a defined dictionary
- **Code** : The Primary section for code to be placed in.

### Empty file example:
```python
# ----------------------------------------------------------------------------------------------------------------------  
# - Package Imports -  
# ----------------------------------------------------------------------------------------------------------------------  
# General Packages  
from __future__ import annotations 
  
# Athena Packages
  
# Local Imports  

# ----------------------------------------------------------------------------------------------------------------------  
# - Support Code -  
# ----------------------------------------------------------------------------------------------------------------------  

# ----------------------------------------------------------------------------------------------------------------------  
# - Code -  
# ----------------------------------------------------------------------------------------------------------------------  
```

##### Empty file example for the root `__init__.py` of a package:
```python
# ----------------------------------------------------------------------------------------------------------------------  
# - Package Imports | <Package name> -  
# ----------------------------------------------------------------------------------------------------------------------  
```

---
## Differences with PEP 8
Although [PEP 8](https://peps.python.org/pep-0008/) is a generally accepted style guide for Python, [Athena's Chaos Drive Code](https://github.com/Athena-Chaos-Driven-Code) doesn't always follow this to the letter.
The following are exceptions to the "normal" PEP 8 style guide.
(PEP 8 is a guide, and is not supposed to be the end-all of how to write Python Code)

### Indentation
Functions that have multiple arguments that don't fit onto a single line, must be split into multiple different lines, where every argument is placed on a separate line.
```python
foo = long_function(
	a="a",
	b="b",
	...
)
```

### Maximum Line Length
The line length is set at 80 characters

### Strict Type annotations
Where possible, always annotate the types of variables, arguments, functions and outputs.

```python
def example_function(a:int, b:str="b") -> None
	return
```

### Naming Styles
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