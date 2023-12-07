Exterior Glass (Dynamic)
================================================

Dynamic Exterior Glazing assemblies represent `SageGlass`_ electrochromic glass products. Each `material`_ has several "tint states" to control glare while maximizing daylight. 

Please note that in the 3D Rhino model, **window assemblies must be modeled as single surfaces**. They should not include multiple surfaces (panes), and they should not contain any solids.

.. figure:: images/matBrowser_dy.png
   :width: 900px
   :align: center

Tint State (Annual Workflows)
----------------------------------------------------

**Tint states** in `annual workflows`_ are usually controlled by a sensor (Automated) but this can be changed in the **"Tint Control" tab (2)**. "Tint Control" has similar options as the **"Shade Control" tab** mentioned `here`_. 

There are four **Types of Tint Controls (3)**: 

- Manual

  - Behavior

    - Default

    - LM83  
 
  - Blinds reopen

    - The following morning 

    - Custom number of days  

- Automated  

- Custom Schedule (CSV File)  (comma separated value) file with 8760 values for every hour of the year. The file format is single column. The dynamic shading state is 0 for wide open and an integer 1, 2 and 3 for dynamic glass with one clear and three tint states.

- Fixed - current point-in-time state - will affect `other workflows`_

Both Manual and Automated uses 2000 lux as **sunlight threshold (4)** for engaging the blinds by default. 


Tint State (Point-In-Time Workflows)
----------------------------------------------------

The state of the tint in `point-in-time workflows`_ is shown on the diagram with a black outline and arrow pointing to the selected tint. Click on another tint to change it's point-in-time state. 

.. figure:: images/matBrowser_dy_click.png
   :width: 600px
   :align: center

.. _SageGlass: https://www.sageglass.com/


.. _other workflows: materials.html#dynamic-material-behavior-based-on-workflow

.. _annual workflows: materials.html#dynamic-material-behavior-based-on-workflow

.. _point-in-time workflows: materials.html#dynamic-material-behavior-based-on-workflow

.. _material: materials.html

.. _here: materials_exteriorGlass.html#shades-control-annual-and-other-workflows
