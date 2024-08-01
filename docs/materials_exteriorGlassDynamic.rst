Exterior Glass (Electrochromic)
================================================

Electrochromic glazing systems consist of two components: 

| **1 -  Electrochromic Glass System**
| **2 -  Tint Control**

Please note that in the 3D Rhino model, **glazing systems must be modeled as single surfaces**. 
They should not include multiple surfaces (e.g. multiple glass panes), and they should not contain any solids. 
The single surface is typically placed at the outside face of glass. 
The two components of the system may be edited using the corresponding tabs (**1-2** below).



.. figure:: images/matBrowser_dy.png
   :width: 900px
   :align: center
   

   
|
Electrochromic Glass System
----------------------------------------------------
Electrochromic glass systems are switchable electrochromic glazing products that change tint to control glare while maintaining views to the outside. Click on a row in the table to select a product.

|
Tint Control
----------------------------------------------------
.. figure:: images/matBrowser_dy_control.png
   :width: 900px
   :align: center
   
|
**Point-in-Time Workflows**

The tint state in `point-in-time workflows`_ is shown in the axon diagram, with a black outline and arrow pointing to the selected tint. Click on another tint to change the point-in-time state or use the **tint (3)** dropdown. 

.. figure:: images/matBrowser_dy_click.png
   :width: 600px
   :align: center

|
**Annual Workflows**

When running `annual workflows`_, the tint state changes from timestep to timestep. The logic controlling this behavior is specified in the **Tint Control tab (2)**.
 


There are four **Types of Tint Control (3)**: 

- **Manual** controls mimic the behavior of dynamic glazings operated by building occupants using manual switches. Note that, apart from override features, dynamic glazing systems are typically automated, making manual control an atypical selection. ClimateStudio offers two flavors of manual control, available via the **Behavior Model (4)** dropdown:

    - **LM-83** controls follow the strictures of dynamic glazing operation according to the IES-NA LM-83 standard. Specifically, dynamic glazings darken when more than 2% of sensors in a room receive direct sunlight (defined as direct horizontal illuminance in excess of 1000 lux). The tint selected is always the lightest one that brings DHI below the threshold. Tints lighten again the instance conditions allow. Note that ClimateStudio's engine knows which window groups are responsible for transmitting sunlight to a sensor, and darkens only responsible groups until the 2% criterion is met. 

    - **Default** controls differ from LM-83 controls in three important respects. First, the trigger is direct *normal* (rather than *horizontal*) illuminance, with an editable threshold defaulting to 2000 lux **(5)**. Second, triggering sensors are limited to portions of the workplane beyond a *permissible depth* from a window. This depth is assessed from room edges adjacent to windows, and can be set via the `occupied area's property panel`_. The default value of 5 feet allows a swath of permissible sun penetration along facade-facing room edges. Any sunlit sensor *not* in this swath will cause the responsible window group to darken. Finally, unlike the LM-83 model, the default control assumes a *latency period* before the glass can lighten again. The default reset occurs the following morning, but the user may specify a longer period of days or weeks.
 

- **Automated** controls mimic the behavior of switchable glazings driven by daylight sensors. Their logic mirrors that of the Default Manual model above, except without a latency period. I.e., the glass tint is lightened immediately once conditions allow.

- **Custom Schedule (CSV File)** controls allow specification of a custom tint schedule via comma-separated value file. The format is a single column of 8760 hourly values with no header. The values indicate the tint state of the glass at each hour, with 0 representing the clearest tint, 1 the next lightest, and so on.

- **Fixed** controls simply set the glass to a fixed tint state for all hours of the year. The tint is assumed to be the point-in-time tint, which is set using the interactive axon diagram (see `above`_).

   
Back to `Materials`_

.. _Materials: materials.html

.. _annual workflows: materials.html#dynamic-materials

.. _point-in-time workflows: materials.html#dynamic-materials

.. _occupied area's property panel: occupiedAreas.html

.. _above: materials_exteriorGlassDynamic.html#tint-control-point-in-time-workflows