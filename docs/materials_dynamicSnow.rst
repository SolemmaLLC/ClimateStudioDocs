Dynamic Snow
================================================

Dynamic Snow `material`_ mimics the reflectivity of snow in winter. 

.. figure:: images/matBrowser_snow.png
   :width: 900px
   :align: center

**Snow Schedule** (1) is calculated based on project location's dry-bulb temperature. Snow will start to appear for consecutive days of below freezing and disappear for consecutive days of warmer temperature. 

The preview of a dynamic snow material is a graph of the snow throughout the year on the x-axis and fraction of snow coverage in the y-axis. Currently the fraction represents the alpha transparency of the snow material in each day of the year. 

If a `point-in-time workflow`_ is selected, the arrow on the x-axis shows the **point-in-time state** selected. This can be changed by selecting a different date in the `Sky`_ Sub-panel. 

This material's `behavior varies slightly based on the workflow selected`_. 


.. _Sky: sky.html

.. _behavior varies slightly based on the workflow selected: materials.html#dynamic-material-behavior-based-on-workflow

.. _material: materials.html

.. _point-in-time workflow: materials.html#dynamic-material-behavior-based-on-workflow
