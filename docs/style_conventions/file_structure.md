# File structure
Generally speaking, a file consists out of three sections:
- **Package Imports** :
	- General Packages : Imports from the standard library or 3rd party packages. Usually has the `from __future__ import annotations` at the top, even though the Python foundation doesn't really know how to implement the feature in full for the future.
	- Athena Packages : Package imports from withing [Athena's Chaos Drive Code](https://github.com/Athena-Chaos-Driven-Code)
	- Local Imports : Imports from the local project itself
- **Support Code** : A section that isn't always present in easy file, as it contains code that the main code relies on, like a regularly occurring string value, or a defined dictionary
- **Code** : The Primary section for code to be placed in.

## Empty file example:
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

## Empty file example for the root `__init__.py` of a package:
```python
# ----------------------------------------------------------------------------------------------------------------------  
# - Package Imports | <Package name> -  
# ----------------------------------------------------------------------------------------------------------------------  
```
