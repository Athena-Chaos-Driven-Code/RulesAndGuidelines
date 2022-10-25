# Stance on 3rd party Packages and Libraries

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

## Python Packages
A full list of accepted 3rd party packages. This list is a limited list, so only the packages noted down here are accepted, if a maintainer or Andreas himself, wants to add a a 3rd party package to a project, this must be reflected into this file.

- [Django](https://pypi.org/project/Django/) : Backend Web-dev
- [DearPyGui](https://pypi.org/project/dearpygui/) : GUI library
	- [DearPyGui_Ext](https://pypi.org/project/dearpygui-ext/)
- [Numpy](https://pypi.org/project/numpy/)
- [Pillow](https://pypi.org/project/Pillow/)
- [scipy](https://pypi.org/project/scipy/)

## Other Software Libraries or Packages
- JavaScript frameworks:
	- React / Angular / ...
- Databases:
	- MariaDB
- Game Engines:
	- Unreal Engine 5