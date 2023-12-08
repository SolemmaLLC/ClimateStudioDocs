Scheduled Material
================================================

Scheduled `material`_ takes any non-dynamic material as input and changes it's behavior based on an hourly year-long schedule. 

.. figure:: images/matBrowser_scheduled.png
   :width: 900px
   :align: center

The preview of a scheduled material is an hourly heat map of the material's schedule with every day of the year on the x-axis and every hour of the day on the y-axis. 
The color of the graph is based on the material's color and the transparency represents the presence / or lack thereof according to the schedule. 

If a `point-in-time workflow`_ is selected, the arrow on the x-axis and the box highlighting the hour shows the **point-in-time state** selected. This can be changed by selecting a different date and time in the `Sky`_ Sub-panel. 

Select any material from the **"Material" tab (1)** by clicking on the materials table. 

To change the schedule and the transparency fraction behavior, use the **"Dynamic Behavior" tab (2)**: 

| **3** - Three different **Transparency Types**: 

  - **Alpha Transparency** uses the fraction as alpha transparency of the material, where 0 is transparent and 1 is opaque. 

  - **BinaryOnOff** rounds the fraction to 0 or 1 and shows the material only on 1. 

  - **MeshFaceScaling** renders the material as is while using the fraction to scale all mesh faces around their first vertex to achieve the global transparent effect. 0 means no mesh faces (scaled by 0 to nonexistent) and 1 means full (original) sized mesh faces. 

| **4** - Click on the **Schedule button** to change schedules in the `schedule editor`_. 

This material's `behavior varies slightly based on the workflow selected`_. 



.. _Sky: sky.html

.. _behavior varies slightly based on the workflow selected: materials.html#dynamic-material-behavior-based-on-workflow

.. _schedule editor: scheduleEditor.html

.. _point-in-time workflow: materials.html#dynamic-material-behavior-based-on-workflow

.. _material: materials.html