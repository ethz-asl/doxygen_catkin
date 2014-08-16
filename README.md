doxygen_catkin
==============

CMake macros for easy doxygen documentation.

This package provides an easy cmake function for creating a Doxygen documentation target using catkin.

## `add_doxygen()` 
This function will find Doxygen and and create a documentation target. 

There are two keyword arguments

* `REQUIRED` -- This will cause a failure if Doxygen is not found by cmake. If this is not added, failing to find Doxygen will simply mean that no documentation is built.
* `NOT_AUTOMATIC` -- If this option is  added, you must build the documentation manually by calling `make doc`. Otherwise the documentation is added to the default build target and built every time you call `make`

## `doxygen-catkin-filegen`
The `add_doxygen()` cmake function expects to find two files in the root directory of your package: `mainpage.dox` and `Doxyfile.in`. To get basic versions of these files, use the utility `doxygen-catkin-filegen` that comes with this package:

```
$ doxygen-catkin-filegen -h
usage: doxygen-catkin-filegen [-h] project

This utility creates a basic doxygen Doxyfile.in and mainpage.dox based on your arguments

positional arguments:
  project     Pretty project name.

optional arguments:
  -h, --help  show this help message and exit
```