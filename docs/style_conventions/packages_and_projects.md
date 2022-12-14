# Packages and Projects
## Name
Package name is written down in **CamelCase** and consists out of two sections: `Athena` and and abstract name for the package's feature

Examples:
- `AthenaLib`   : Collection of boilerplate code
- `AthenaColor` : Console coloring

## Version
Version strings of packages will follow [Semantic Versioning 2.0.0](https://semver.org/spec/v2.0.0.html) guideline of: `Major.Minor.Patch`
- Major : Changes to the API, that are incompatible with previous states of the code 
- Minor : Additions of functionality, that don't cause compatibility issues.
- Patch : Bug Fixes

## Files and Folders
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
โ๐res
โ   โ๐images
โ   โ๐data
โ
โ๐docs
โ
โ๐src (Marked in PyCharm as the Source root)
โ   โ๐Athena<Package>
โ	      โ๐data (Static data like commonly used strings, enum, etc...)
โ	      โ๐functions (Stand alone functions, decorators, and generators)
โ	      โ๐objects (Classes)
โ	      โ๐__init__.py (root imports)
โ
โ๐tests (collection of tests, different sub folders mark different subjects)
โ
โ๐.gitignore
โ๐readme.md
โ๐setup.py	

```
