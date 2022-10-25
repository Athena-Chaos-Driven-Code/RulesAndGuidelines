# Rules and Guidelines

A collection of rules and guidelines for [Athena's Chaos Drive Code](https://github.com/Athena-Chaos-Driven-Code) related repo's and projects

## Supported Python Versions
- Only support the most recent stable version of Python:
	- Currently this is: [v 3.11.0](https://www.python.org/downloads/release/python-3110/) 
		- If the version of Python is still in an early release state, or the version has just come out, updating all the packages might take some time

- Exceptions to this rule:
	- [AthenaColor](https://github.com/Athena-Chaos-Driven-Code/AthenaColor), which is supported from 3.7 and onwards

---

## Stance on 3rd party Packages and Libraries

Generally speaking, [Athena's Chaos Drive Code](https://github.com/Athena-Chaos-Driven-Code) will try to limit itself to the standard library of a given programming language.
This "rule" came from the idea that by approaching a problem with a self built solution, Andreas would get a deeper understanding of how certain programing concepts, or systems work. This later evolved into a general concept of: "Developing and understanding the logic behind a certain tool is better than just accepting that 'magic' will solve the problem".

Although, reinventing the wheel is an accepted stance, there are certain concepts and systems that Andreas doesn't want to develop from the ground up.
In general, this means that there are a couple of sections of types of packages or systems that are always allowed as a 3rd party dependency:
- Security related packages : Anything that involves password management, OAUTH, or anything involving user data security
- GUI Libraries: Anything involving GUI
- Math related
- Packages that are generally accepted as "semi-standard" packages
- Databases and database connectors
- Game Engines

### Python Packages
A full list of accepted 3rd party packages. This list is a limited list, so only the packages noted down here are accepted, if a maintainer or Andreas himself, wants to add a a 3rd party package to a project, this must be reflected into this file.

- [Django](https://pypi.org/project/Django/) : Backend Web-dev
- [DearPyGui](https://pypi.org/project/dearpygui/) : GUI library
	- [DearPyGui_Ext](https://pypi.org/project/dearpygui-ext/)
- [Numpy](https://pypi.org/project/numpy/)
- [Pillow](https://pypi.org/project/Pillow/)
- [scipy](https://pypi.org/project/scipy/)

### Other Software Libraries or Packages
- JavaScript frameworks:
	- React / Angular / ...
- Databases:
	- MariaDB
- Game Engines:
	- Unreal Engine 5

---

## Style Conventions:
### Packages and Projects
Package name: `Athena<feature of package>`

Version strings of packages will follow [Semantic Versioning 2.0.0](https://semver.org/spec/v2.0.0.html) guideline of: `Major.Minor.Patch`
- Major : Changes to the API, that are incompatible with previous states of the code 
- Minor : Additions of functionality, that don't cause compatibility issues.
- Patch : Bug Fixes

files and folders within a package are to named with the **snake_case** convention
- This rule does not count for the folder that is the root of the Package, which must be in **CamelCase** convention

Project setup:
```
├📁res
│   ├📁images
│   ├📁data
├📁src (Marked in PyCharm as the Source root)
│   ├📁Athena<Package>
│	│	├📁data (Static data like commonly used strings, enum, etc...)
│	│	├📁functions (Stand alone functions, decorators, and generators)
│	│	├📁objests (Classes)
│   ├📄__init__.py (root imports)
├📁tests
├📄.gitignore
├📄README.md
├📄setup.py		

```

### Python 
#### File
Generally speaking, a `.py` file consists out of three sections:
- **Package Imports** :
	- General Packages : Imports from the standard library or 3rd party packages. Usually has the `from __future__ import annotations` at the top, even though the Python foundation doesn't really know how to implement the feature in full for the future.
	- Athena Packages : Package imports from withing [Athena's Chaos Drive Code](https://github.com/Athena-Chaos-Driven-Code)
	- Local Imports : Imports from the local project itself
- **Support Code** : A section that isn't always present in easy file, as it contains code that the main code relies on, like a regularly occurring string value, or a defined dictionary
- **Code** : The Primary section for code to be placed in.

##### Empty file example:
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

## Git Commit Messages:

Git commit message format:
| Subject                                                             | Git Title          |
| ------------------------------------------------------------------- | ------------------ |
| Feature addition                                                    | `Feat : ...`       |
| Documentation                                                       | `Docs : ...`       |
| Bug fix                                                             | `Fix : ...`        |
| Neither a fix or a feature addition, but a rework of a given system | `Refactor : ...`   |
| Performance improvements                                            | `Perfomance : ...` |
| Version Bump                                                        | `Bump : ...`       |
| Update to the .gitignore file                                       | `GitIgnore : ...`  |

Git commit note format:
- Twitch redeemable for "*make Andreas save and/or commit*":
```
This commit was made possible by: ...
```

- Twitch redeemable for "*make Andreas save and/or commit, with custom message*":
```
This commit was made possible by: ...
With the following message : "..."
```

---

