Scheduled Material
================================================

Scheduled materials are materials that appear or disappear based on an annual schedule.

.. figure:: images/matBrowser_scheduled.png
   :width: 900px
   :align: center

|
Material
----------------------
To select a material, use the *Material* tab (**1**) and select a row in the table. If you have created custom Radiance materials (see `here`_), you can access them via the library dropdown (**4**). 

Dynamic Behavior
-----------------------
To select a schedule, use the *Dynamic Behavior* tab (**2**) and browse for a schedule using the schedule button (**6**), which opens a `schedule editor`_.

The preview shows an hourly map of the material's schedule, with days of the year on the x-axis and hours of the day on the y-axis. The color of the graph is based on the material's reflection color, while the transparency represents its presence (or lack thereof) according to the schedule. 

If a point-in-time workflow (`Rendering`_ or `Point-in-Time Illuminance`_) is active, the arrow on the x-axis and the box highlighting the hour indicates the **point-in-time state** used by the simulation. This depends on the date and time in the `Sky`_ sub-panel. 

Annual workflows (`Annual Glare`_, `Radiation Maps`_, and *LEED* / *Custom* / *EN* / *BREEAM 4b* `Daylight Availability`_ runs) use the schedule to set the behavior of the material at each hourly timestep. In `View`_, *Daylight Factor*, and *BREEAM 4a/c* daylight simulations, the material is assumed to be present if the Rhino layer is on.

When the schedule's value is 0, the material is absent. When the schedule's value is 1, and material is present. Fractional values between 0 and 1 are interpreted according to the **Transparency Type (5)** dropdown: 

  - **Alpha Transparency** uses the fraction as the material's alpha channel, with 0 being fully transparent and 1 fully opaque. 

  - **BinaryOnOff** assumes full opacity whenever the fraction is greater than 0. 

  - **MeshFaceScaling** uses the fraction to scale each mesh face about its first vertex. For example, a value of 0.5 shrinks faces by a factor of 2, while a value of 0 causes faces to disappear completely. The maximum fraction is 1, meaning elements cannot grow beyond their modeled size. MeshFaceScaling may be useful for dynamic elements like deciduous leaves that grow or shrink throughout the year. 


Back to `Materials`_

.. _here: customRadianceMaterials.html

.. _Materials: materials.html

.. _Sky: sky.html

.. _behavior varies slightly based on the workflow selected: materials.html#dynamic-material-behavior-based-on-workflow

.. _schedule editor: scheduleEditor.html

.. _View: viewAnalysis.html
.. _Annual Glare: annualGlare.html
.. _Daylight Availability: daylightAvailability.html
.. _Radiation Maps: radiationMap.html
.. _Rendering: radianceRender.html
.. _Point-in-Time Illuminance: illuminance.html
