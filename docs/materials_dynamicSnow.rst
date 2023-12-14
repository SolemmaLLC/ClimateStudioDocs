Dynamic Snow
================================================

Dynamic snow materials mimic the reflectivity of snow in winter. 

.. figure:: images/matBrowser_snow.png
   :width: 900px
   :align: center
   
|
The **Snow Schedule (1)** is calculated based on the `project location's`_ weather file. The algorithm is based on Dry Bulb Temperature (DBT) -- with snow beginning to accumulate on consecutive days with below-freezing temperatures, and beginning melt on consecutive days with above-freezing temperatures. Precipitation data are not currently considered.

The preview graph shows snow coverage throughout the year, with the date on the x-axis and coverage fraction on the y-axis. Fractions between 0 and 1 are interpreted using the material's alpha channel (with 0 being fully transparent, at 1 fully opaque).

If a `point-in-time workflow`_ is selected, the arrow on the x-axis shows the **point-in-time state** selected. This depends on the date in the `Sky`_ sub-panel. `Annual workflows`_ use the schedule to set the behavior of the material at each hourly timestep. 

Back to `Materials`_

.. _Materials: materials.html

.. _Sky: sky.html

.. _material: materials.html

.. _point-in-time workflow: materials.html#dynamic-materials

.. _Annual workflows: materials.html#dynamic-materials

.. _project location's: location.html