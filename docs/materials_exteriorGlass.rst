Exterior Glass
================================================

Exterior glazing systems consist of three components: 

| **1 -  Glass Material**
| **2 -  Shade Material**
| **3 -  Shade Control**

Please note that in the 3D Rhino model, **glazing systems must be modeled as single surfaces**. They should not include multiple surfaces (e.g. multiple glass panes), and they should not contain any solids. The single surface is typically placed at the outside face of glass. When a shade material is specified, ClimateStudio generates shading surfaces automatically -- inset from the glass. This applies to all surfaces on the Rhino layer. The three components of the system may be edited using the corresponding tabs (1-3 below).

.. figure:: images/matBrowser_ex_glass.png
   :width: 900px
   :align: center

|
Glass Material
----------------------------------------------------
Glass materials (typically IGUs) are sourced from the International Glazing Database (IGDB). The default library contains a collection of hundreds of units, spanning a range of performance characteristics. Click on a row in the glazing table to change the selection.

Shade Material
----------------------------------------------------
Shading systems and their operation are simulated by the `Daylight Availability`_ and `Annual Glare`_ workflows when calculating hourly (il)luminance distributions. In many cases, the inclusion of dynamic shading is not optional. The calculation of Spatial Daylight Autonomy (sDA) and eligibility for the LEED v4 Daylight credit (Option 1) require dynamic shading to be modeled on all exterior windows. 

Open the **Shade Material tab (2)**  to access the shade materials table. Click on a row to change the selection. Windows without shades may be modeled by selecting the "No Shade" option.

.. figure:: images/matBrowser_ex_shade.png
   :width: 900px
   :align: center

 
|
Shade Control (Point-In-Time Workflows)
----------------------------------------------------

The position of the shade in `point-in-time workflows`_ is displayed and set using the interactive axon diagram. Click on the shade to change its point-in-time state.


.. figure:: images/matBrowser_ex_click.png
   :width: 600px
   :align: center

|
Shade Control (Annual Workflows)
----------------------------------------------------
When running `annual workflows`_, the position of each shade changes from timestep to timestep. The logic controlling this behavior is specified in the **Shade Control tab (3)**.

.. figure:: images/matBrowser_ex_Control.png
   :width: 900px
   :align: center

There are four **Types of Shade Control (4)**: 

- **Manual** controls mimic the behavior of shades operated by building occupants. ClimateStudio offers two flavors of manual control, available via the **Behavior Model (5)** dropdown:

    - **LM-83** controls follow the strictures of blind operation according to the IES-NA LM-83 standard. Specifically, blinds close when more than 2% of sensors in a room receive direct sunlight (defined as direct horizontal illuminance in excess of 1000 lux). Blinds reopen immediately once the condition is no longer met. Note that ClimateStudio's engine knows which blinds groups are responsible for transmitting sunlight to a sensor, and closes only responsible groups until the 2% criterion is met. 

    - **Default** controls differ from LM-83 controls in three important respects. First, the trigger is direct *normal* (rather than *horizontal*) illuminance, with an editable threshold defaulting to 2000 lux **(7)**. Second, triggering sensors are limited to portions of the workplane beyond a *permissible depth* from a window. This depth is assessed from room edges adjacent to windows, and can be set via the `occupied area's property panel`_. The default value of 5 feet allows a swath of permissible sun penetration along facade-facing room edges. Any sunlit sensor *not* in this swath will cause the responsible blinds group to close. Finally, unlike the LM-83 model, the default control assumes a *latency period* before the **blinds reopen (6)**. The default reopening occurs the following morning, but the user may specify a longer period of days or weeks.
 

- **Automated** controls mimic the behavior of motorized blinds driven by daylight sensors. Their logic mirrors that of the Default Manual model above, except without a latency period. I.e., blinds are reopened immediately once the trigger condition is no longer met. 

- **Custom Schedule (CSV File)** controls allow specification of a custom blinds schedule via comma-separated value file. The format is a single column of 8760 hourly values with no header. The values indicate the position of the shade at each hour, with 0 for open and 1 for closed.

- **Fixed** controls simply set the shade to a fixed position for all hours of the year. The position is assumed to be the point-in-time position, which is set using the interactive axon diagram (see `above`_).


Back to `Materials`_.

.. _annual workflows: materials.html#dynamic-materials

.. _point-in-time workflows: materials.html#dynamic-materials

.. _Materials: materials.html

.. _Daylight Availability: daylightAvailability.html

.. _Annual Glare: annualGlare.html

.. _occupied area's property panel: occupiedAreas.html

.. _above: materials_exteriorGlass.html#shade-control-point-in-time-workflows