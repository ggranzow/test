# Source Code and Instructions for Generating Instructions for the Capstone Weather Project

This directory contains source code for generating the instructions for the Capstone Weather project, [exercises/capstone_weather/instructions.html](https://github.com/enthought/class-material/blob/dev/exercises/capstone_weather/instructions.html.)

The source for the instructions is in the reStructuredText file [project.rst](https://github.com/enthought/class-material/blob/dev/capstone_weather/project.rst).

Creating the instructions file involves three steps:

1. Convert the `reStructuredText` file, `project.rst`, to `html`.
2. Modify the `html` file so the visibility of the "tips" in the instructions can be toggled by the student reading the instructions.
3. Move the modified html file (which is the `instructions.html` file) to the `exercises/capstone_weather` folder.

## Some preliminary steps

In order to accomplish the first step, you need to be in an environment where `rst2html` is installed.
The `cm` environment, whose creation is described [here](https://github.com/enthought/class-material/blob/dev/ci/QUICKSTART.md) would work.
Or you can use the standard `python-class` environment used for our classes.
Assuming that you have created the `cm` environment, you can activate it using:

`edm shell -e cm`

Next you should use `cd` to change directory to the `capstone_weather` directory in your local copy of the `class-materials` repository (where this `README.md` file and the `project.rst` file are found).

## Creating the `instructions.html` file

The three steps in the numbered list above can be accomplished by executing the following (on windows use backslashes instead of forward slashes):

    rst2html project.rst build/project.html
    python hidetips.py
    mv build/instructions.html ../exercises/capstone_weather/

## A note about images

The instructions include images.
These images are in [exercises/capstone_weather/images](https://github.com/enthought/class-material/blob/dev/capstone_weather/images).

The images were created using a screen capture tool.
The windows that were captured were created by running [figures.py](https://github.com/enthought/class-material/blob/dev/capstone_weather/figures.py)

## Creating the map of the United States used in the enhancements.

The map of the united states in [exercises/capstone_weather/data/mapUSA.png](https://github.com/enthought/class-material/blob/dev/exercises/capstone_weather/mapUSA.png) was created using [create_map.py](https://github.com/enthought/class-material/blob/dev/capstone_weather/create_map.py).

This script requires the `cartopy` module.  The `python-class` environment includes `cartopy`.

