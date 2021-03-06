Emperor ChangeLog
=================

Emperor 0.9.3-dev (changes since Emperor 0.9.2 go here)
-------------------------------------------------------

* Category names are no longer trimmed to 25 characters in the user interface.
* Change the minimum percent required to display a plot to be greater than 0.01 instead of 0.5.
* The percent explained by each of the axes is now formatted as a floating point number with two digits in the mantissa.
* The `Key` tab now uses all the available space on screen.
* Improve mouse sensitivity to rotate, pan, zoom-in and zoom out in the 3D plot.
* Emperor is now hosted under the biocore GitHub organization.
* Add toggle visible button (`Invert Selected`) under the `Visibility` tab, this button will change hidden categories to visible and vice-versa.
* Supports both NumPy 1.7 and 1.8.
* Depends on scikit-bio-dev.
* Emperor provides a Python object that is IPython aware (emperor.Emperor) that will display a usable plot from within the IPython notebook.

*Bug Fixes*

* Fixed problem where coordinate files with large values (greater than 100) would not be displayed on screen.
* Fixed problem that prevented the user from scrolling through the categories in the user interface.
* Clean-up the layout of the user interface so it's cleaner and consistent.
* Fix problem where long category names would alter the layout of the interface.
* Fix inability to write an 'E' character in the Filename field when exporting an svg.

*New Features*

* Support both classic and [scikit-bio](http://scikit-bio.org)'s coordinate formats.

Emperor 0.9.3 (5 Dec 2013)
--------------------------

* `Use gradient colors` checkbox is now found under the `Colors` tab.
* Merge the `Options` and `View` tabs; additionally the global opacity slider and global scale slider were moved to their respective tabs.
* `Use gradient colors` checkbox now uses the standard blue -> red color gradient
* Add Emperor to the Python Package Index, now you can install Emperor running `pip install emperor`.
* Remove dependency on QIIME and PyCogent.
* Emperor now depends on qcli and Numpy.

*Bug Fixes*

* Add more meaningful error message for biplots when the contingency table passed included only one row.

Emperor 0.9.2 (24 Oct 2013)
---------------------------

*Bug Fixes*

* Fixes bug where files named `procrustes_results.txt` would not be ignored in a plot comparison.


Emperor 0.9.1 (21 Oct 2013)
---------------------------

*New features*

* Scientific notation is now taken into account in the GUI for scientific coloring.
* GUI is usable in mobile devices that support WebGL.
* User documentation: tutorial, installation instructions, GUI description, etc.
* Ability to make plot comparisons (very useful for procrustes analysis plots).
* The user can select the number of axes to be considered in the GUI and re-plot using lower axes; this is, for example: PC3 vs PC4 vs PC10.
* In missing_custom_axes_values you can reference other column within the mapping file to place the samples without numeric values at different points in the gradient.
* Parallel plots functionality.
* Separated out some options to the View menu.
* The "Colors" tab now has a selector, which allows to use the arrows to move between categories.
* Default coloring scheme is discrete.
* Add color pickers for the axes and axes labels.
* To take a screenshot (PNG) of your current visualization you can press `ctrl+p`.
* Export to SVG your visualization.
* Emperor now relies on QIIME 1.7.0.
* Added option `--number_of_segments` to control the quality of all spheres
* Labels for biplots now have a color picker.
* Add color pickers for connecting bars in coordinate comparison plots.
* Add option to select a master set of coordinates when making a comparison plot.
* Adds a feature to negate axes. With this feature you can negate the coordinates of each data point. As a result, the spheres and/or edges will be adjusted appropriately. 
* Minor additions to the separator controller for the side bar.
* As of 308629f550ff3e108903d3bcf1ce76ce85f4cb96 Emperor is now released under a BSD license.


*Bug Fixes*

* Fixes recenter camera not working.
* Category names are sorted alphabetically.
* Category names with non-alphanumeric characters are colored correctly now.
* Biplots checkbox now accurately reflects status of biplot visiblity rather than opposite.
* Comparison bars checkbox now accurately reflects status of the visiblity rather than opposite.
* Scaling by percent explained now works with vectors and coordinate comparison plots.
* Fixed bug where only the first bars in coordinate comparison plots could be hidden.
* Improved documentation for saving and exporting images.
* Emperor now fails graciously when WebGL is not enabled and gives you a few suggestions on how to get it to work.



Emperor 0.9.0 (14 May 2013)
---------------------------

*New features*:

* Intuitive and modern graphical user interface.
* Simple workflow to modify the color of a sample/label from the user interface.
* Color the labels for the samples by a category in the mapping file.
* Scale the elements in the plot by the percentage explained from the user interface.
* Notify the user when values will be removed from the input files.
* Search for a sample name from the graphical user interface.
* Show a selector in the plot when double-clicking a sample name.
* Show and hide samples by a category in the mapping file.
* Change the opacity of spheres/ellipses from the graphical user interface.
* Change the size of a sphere from the graphical user interface.
* Biplots can be created with a custom axis.
* The color of the biplot spheres can now be changed from the user interface.
* Extensive script usage testing
* Addition of contextualized error messages.
* Reduced output size for datasets with rich mapping files.

*Performance improvements*:

* Improved performance and responsiveness from the graphical user interface.
* Superior graphics quality; elements are rendered in the graphics card not in the CPU.
* Enhanced performance to create the output files.
