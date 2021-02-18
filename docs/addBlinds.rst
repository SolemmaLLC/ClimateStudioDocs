
Add Blinds
================================================
Several workflows including `Daylight Availability`_  support the setting of dynamic shading systems, such as fabric shades or switchable glazings. Specifying such a system requires identifying windows that have a dynamic shading system and specifying a shading type and control strategy for each window. The process is initiated via the Add Blinds subpanel. Left-click on the Add Blind button and select one or more window surfaces.

.. _Daylight Availability: daylightAvailability.html



.. figure:: images/AddBlinds.jpg
   :width: 900px
   :align: center

In the example below, three window surfaces, one in the conference room and two in the corner office have been selected. 

	**Tip:** A quick way to select mutiple windows is to pick all objects on the *glazing* layer.

.. figure:: images/blinds1.png
   :width: 900px
   :align: center
   
Once all window surfaces with a shading system have been selected, the *Edit Dynamic Windows* panel opens. 

**Type:** As shown below, the dialogue allows setting the shading type and control strategy, *operable blinds* and *dynamic glass.* For both cases, ClimateStudio comes with a list of actual materials. For operable blinds, it is assumed that the shading system is either fully opened or fully closed. For dynamic glass, several intermediate tint states, as provided by the manufacturer, are supported. In the example below, Halio Black comes with one clear and six tint states ranging from 50.6% to 0.1% visual light transmittance.

**Schedule:** The schedule input sets the dynamic shading control strategy for the shading, i.e when it is opened or closed.  The following controls are currently supported:

- **Default (LEEDv4 2% Rule):** According to this control algorithm, a shading system is closed if more than 2% of an occupied area associated with a window is illuminated by more than 1000lux of direct sunlight. For dynamic glass, the transmittance of the glass is lowered until either the 1000lux criterion is not met anymore or the glass is in its darkest tint state.

- **Custom (CSV file):** Alternatively, the user can provide a CSV (comma seperated value ) file with 8760 values for every hour of the year. The file format is single column. The dynamic shading state is 0 for wide open and an integer depending on the number of shading states supported, i.e. 1 for up/down blinds or 1, 2 and 3 for dynamic glass with one clear and three tinted states.

.. figure:: images/blinds2.png
   :width: 900px
   :align: center
   
Once all dynamic shading systems have been specified, they appear in the *Add Blinds* subpanel table as shown below. Same as *Occupied Areas,* the different window shading systems can be organized via tags and selections can be edited.

.. figure:: images/blinds3.png
   :width: 900px
   :align: center
   
Simulation Details2,3,
   :align: center









