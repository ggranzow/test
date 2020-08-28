# Source Code and Instructions for Generating Instructions for the Capstone Weather Project

This directory contains source code for generating the instructions for the Capstone Weather project, [exercises/capstone_weather/instructions.html](https://github.com/enthought/class-material/blob/dev/exercises/capstone_weather/instructions.html).

The source for the instructions is in the reStructuredText file [project.rst](https://github.com/enthought/class-material/blob/dev/capstone_weather/project.rst).

Creating the `instructions.html` file involves three steps:

1. Convert the _reStructuredText_ file, `project.rst`, to _html_.
2. Modify the html file so the visibility of the "tips" in the instructions can be toggled by the student reading the instructions.
3. Move the modified html file (which is the `instructions.html` file) to the `exercises/capstone_weather` folder.

These steps are described in more detail below.
If you intend to modify the project instructions, you should edit the [project.rst](https://github.com/enthought/class-material/blob/dev/capstone_weather/project.rst) file, then recreate the [instructions.html](https://github.com/enthought/class-material/blob/dev/exercises/capstone_weather/instructions.html) file by completing the prescribed steps.

## Prerequisite steps

In order to accomplish the first step, you need to be in an environment where `rst2html` is installed.
`rst2html` can be installed using:

`pip install rst2html`

Next, use `cd` to change directory to the `capstone_weather` directory in your local copy of the `class-materials` repository (where this `README.md` file and the `project.rst` and `hidetips.py` files are found).

Finally, create a `build` directory to contain the intermediate and final files created during the process using:

`mkdir build`

## Creating the `instructions.html` file

After installing `rst2html` and changing to the correct directory, the three steps in the numbered list above can be accomplished by executing the following:

    rst2html project.rst build/project.html
    python hidetips.py
    mv build/instructions.html ../exercises/capstone_weather/

## A note about images

The instructions include images.
These images are in [exercises/capstone_weather/images](https://github.com/enthought/class-material/blob/dev/capstone_weather/images).

The images were created using a screen capture tool.
The windows that were captured were created by running [figures.py](https://github.com/enthought/class-material/blob/dev/capstone_weather/figures.py).

## Creating the map of the United States used in the enhancements.

The map of the United States in [exercises/capstone_weather/data/mapUSA.png](https://github.com/enthought/class-material/blob/dev/exercises/capstone_weather/mapUSA.png) was created using [create_map.py](https://github.com/enthought/class-material/blob/dev/capstone_weather/create_map.py).

[create_map.py](https://github.com/enthought/class-material/blob/dev/capstone_weather/create_map.py) requires the `cartopy` module.  The `python-class` environment used in our classes includes `cartopy`.

