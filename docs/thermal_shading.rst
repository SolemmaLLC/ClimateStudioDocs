Shading
================
Shading surfaces may represent an overhang or parts of a neighboring building that shade `thermal zone`_ or `window`_ objects. 
EnergyPlus will create a shading mask for each window and all shading surfaces. 
This process is both slow, as well as somewhat unstable, 
so it is recommended that shading surfaces are assigned somewhat selectively. 
For example, in the urban massing model below, 
shading surfaces are the overhangs as well as walls from neighboring buildings that face the apartment building in the center. 

.. _thermal zone: thermal_zone.html
.. _window: thermal_window.html

.. figure:: images/addObjects11.png
   :width: 900px
   :align: center
