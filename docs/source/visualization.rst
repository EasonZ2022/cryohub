Visualization
===

In cryoHub, we have created some pre-defined widget to display images and objects.
We will continue to work on them and add new widgets.

Visualization will be shown in the ``Visualization`` tab in each job card:
[image]

In the file system, an optional folder can be created with the name ``postprocess``
under the job folder (e.g. ``./Class2D/job016/postprocess``). cryoHub will try to render
everything in this folder to the ``Visualization`` tab in the job card with the pre-defined
widgets based on their **file names**.

Developers can use the ``postprocess`` or ``file_postprocess`` field in the yaml file
to call a secondary command to save images and/or objects with the desired file names
for visualization.


Plain images
------------

``File name``: any name other than the ones will be rendered through other widgets.

``File format``: any image format.

``Display``: plain images displayed sequentially with a fixed width. [image]


Images in a list
------------

``File name``: ``ls-*`` as the prefix (e.g. ``ls-aa.png``)

``File format``: any image format.

``Display``: a list to select the image to display. The list contains the file names
(without the extension and without the prefix ``ls-``) of the images. [image]



Visualization in groups
------------

``File name``: ``itxxx-*`` as the prefix (e.g. ``it001-aa.png``, ``it016-aa.png``, ``it004-ls-aa.png``)

``File format``: any format that is useable for other widgets.

``Display``: the objects with the same prefix will be displayed.
This widgets can be combined with others (e.g. ``it001-ls-*``). [image]
