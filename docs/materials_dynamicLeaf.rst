Dynamic Leaf
================================================

Dynamic leaf materials are species-specific foliage materials that change throughout the year. Their data are sourced from measurements provided by `"Simulating the Impact of Deciduous Trees on Energy, Daylight, and Visual Comfort," Pan and Jakubiec (2022)`_. 

.. figure:: images/matBrowser_leaf.png
   :width: 900px
   :align: center
   
|
The **Leaf Schedule (1)** is calculated using the `project location's`_ length of day (latitude), which determines when the leaves change color and size. The autumn color gradient is achieved by interpolation between measured summer and fall colors. The interpolated hues may or may not correspond to the species' actual color sequence. 

The plotted graph shows leaf color throughout the year on the x-axis, and leaf size on the y-axis (where 0 indicates no leaf, and 1 a fully-sized leaf). Intermediate sizes are achieved by scaling each leaf face about its first vertex, to represent partial states of growth or fall.

If a `point-in-time workflow`_ is selected, an arrow on the x-axis indicates the current day in the schedule. This depends on the date in the `Sky`_ sub-panel. `Annual workflows`_ use the schedule to set the behavior of the material at each hourly timestep. 

 

.. _Sky: sky.html

.. _behavior varies slightly based on the workflow selected: materials.html#dynamic-materials

.. _"Simulating the Impact of Deciduous Trees on Energy, Daylight, and Visual Comfort," Pan and Jakubiec (2022): https://publications.ibpsa.org/proceedings/esim/2022/papers/esim2022_251.pdf

|
Back to `Materials`_

.. _Materials: materials.html

.. _point-in-time workflow: materials.html#dynamic-materials

.. _Annual workflows: materials.html#dynamic-materials

.. _project location's: location.html
