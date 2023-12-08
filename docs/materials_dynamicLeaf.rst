Dynamic Leaf
================================================

Dynamic Leaf `materials`_ are created from species-specific measured data provided in this paper: `Simulating the Impact of Deciduous Trees on Energy, Daylight, and Visual Comfort`_. 

.. figure:: images/matBrowser_leaf.png
   :width: 900px
   :align: center
   
With the measured data for **leaf colors in summer and fall**, we interpolate by hue for a transition gradient between the two colors through the seasons. 

**Leaf Schedule (1)** is calculated based on project location's length of day (latitude) and determines when the leaves change color and size. 

The preview of a dynamic leaf material is a graph of leaf color throughout the year on the x-axis with leaf size from none to full size on the y-axis. Leaf mesh triangles are scaled based on leaf size to achieve gradual changes in density from leaf growth to leaf fall. 

If a `point-in-time workflow`_ is selected, the arrow on the x-axis shows the **point-in-time state** selected. This can be changed by selecting a different date in the `Sky`_ Sub-panel. 

This material's `behavior varies slightly based on the workflow selected`_. 

.. _Sky: sky.html

.. _behavior varies slightly based on the workflow selected: materials.html#dynamic-material-behavior-based-on-workflow

.. _Simulating the Impact of Deciduous Trees on Energy, Daylight, and Visual Comfort: https://publications.ibpsa.org/proceedings/esim/2022/papers/esim2022_251.pdf

.. _materials: materials.html

.. _point-in-time workflow: materials.html#dynamic-material-behavior-based-on-workflow
