# Requirements

As a bioimage analyst I would like to be able to examine 3D images
interactively so that I can visually confirm that my scripts for transforming
and extracting quantitative data from them are sane.

However, creating a one-size fits all 3D visualiser may not be possible. I
would therefore like a framework that allows me to create custom 3D visualisers
in five to ten lines of code.

In its most basic form the visualiser should have built-in support for
rotation, translation, zooming and z-clipping. It should also be capable of
exporting (ray-traced) images of the current view and be able to record movies.

The framework should be able to support 3D volume rendering as well as
displaying surfaces and surfaces with properties projected onto them.

Ideally there should be clear separation of concerns between the module
responsible for visualisation and any modules for parsing and transforming
data.  In other words the visualisation module should only have to be able to
load 3D arrays and meshes. This also means that modules responsible for data
transformations, such as converting 3D arrays into meshes, should be able to
work independently of the visualiser in headless mode.

The framework should expose an API that makes it possible and easy to build
interactive scripting interfaces. For example one could imagine wanting to
create a scripting interface similar to that present in PyMol. Another example
might be the desire to create a modal keyboard interface similar to that in
``vim``.


## Functionality for a minimum loveable product

- Convert directory with png images to a 3D array
- Display the 3D array as volume in the visualiser
- Ability to rotate and z-clip the view in the visualiser
