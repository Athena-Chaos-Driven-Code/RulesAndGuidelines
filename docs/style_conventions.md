# Style Conventions:
## Packages and Projects
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
├📁docs
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