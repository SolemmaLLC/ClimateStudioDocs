
Materials
================================================
The Materials panel is used to assign materials for lighting simulation. Each object in a Rhino model is located on a layer. ClimateStudio uses these layers to assign material properties to scene objects. When setting up a model, objects with different material properties should be placed on different layers, with each layer given an appropriate material. Objects on layers without an assigned material are **ignored** by all lighting simulations. 

.. figure:: images/subPanel_materials.png
   :width: 900px
   :align: center

To assign a layer material, left-click on the material row next to the layer. An Edit Layer Material dialog will appear, letting you browse through ClimateStudio's extensive library of measured materials:

Material Browser
----------------------------------------------------

.. figure:: images/matBrowser.png
   :width: 900px
   :align: center

The library is divided into eight categories: 

- `Exterior Glass`_
- `Exterior Glass (Dynamic)`_
- `Exterior Glass (Translucent Insulating)`_
- `Interior Glass`_
- Other
- `Dynamic Leaf`_
- `Dynamic Snow`_
- `Scheduled Material`_

.. _Exterior Glass: materials_exteriorGlass.html
.. _Exterior Glass (Dynamic): materials_exteriorGlassDynamic.html
.. _Exterior Glass (Translucent Insulating): materials_exteriorGlassTranslucent.html
.. _Interior Glass: materials_interiorGlass.html
.. _Dynamic Leaf: materials_dynamicLeaf.html
.. _Dynamic Snow: materials_dynamicSnow.html
.. _Scheduled Material: materials_scheduledMaterial.html

Use the category dropdown (1) to switch between types of materials. 

Use library dropdown (2) to choose between different libraries or (for expert users) manage your `custom Radiance materials`_ libraries with the library button (3). 

The top section of this dialog shows visualization, diagrams, and properties (physical characteristics and source data) of the material selected (4). 

Below the preview section are the tabs (5) controlling what is displayed in the table below (7).  

Use the search box (6) to filter your options. The columns in the table (7) are sortable, which facilitates ordering items by material property. 

Once selection is complete, choose either to "Cancel" (will not apply change), "Clear" (removes all material from selected layers), or "Select" (applies selected material to all selected layers) (8) to close the dialog.   


Dynamic Material Behavior Based on Workflow
----------------------------------------------------

Dynamic Materials like  `Dynamic Leaf`_, `Dynamic Snow`_, `Scheduled Material`_, `Exterior Glass (Dynamic)`_, and `Exterior Glass (Translucent Insulating)`_ behave differs depending on the workflow. 

There are three types of workflows: 

- **Point-In-Time workflows**

  - `Point-in-time Illuminance`_

  - `Radiance Render`_

- **Annual workflows**

  - `Annual Glare`_

  - `Radiation Map`_

  - `Daylight Availability`_

    - all LEED (v4.1 Option 1, v4.0 Option 1, v4 Option 2)

    - BREEAM UK 4.b

    - BREEAM International 4b

    - EN 17037

    - Custom

- **Other workflows**

  - `View Analysis`_ 

  - `Daylight Availability`_

    - BREEAM UK 4.a, 4.c (Healthcare only)

    - BREEAM International 4.a

    - Daylight Factor




**Point-In-Time workflows**

  | `Dynamic Leaf`_ , `Dynamic Snow`_ and `Scheduled Material`_ will behave based on the current schedule and the specific date and or time selected in the `Sky`_ Sub-panel. 

  | `Exterior Glass Shades`_ and `Exterior Glass (Dynamic) Tint`_ will behave based on the selected point-in-time state. 

**Annual workflows**

  | `Dynamic Leaf`_ , `Dynamic Snow`_ and `Scheduled Material`_  will behave based on the schedule and simulation time-step. 

  | `Exterior Glass Shades (annual)`_ and `Exterior Glass (Dynamic) Tint (annual)`_ will behave based on the their respective control settings. 

**Other workflows** are "timeless" thus neither schedule nor control will apply be default

  | `Dynamic Leaf`_ , `Dynamic Snow`_ and `Scheduled Material`_  state is set only by layer visibility. The schedule is completely ignored. 

  | `Exterior Glass Shades`_ and `Exterior Glass (Dynamic) Tint`_ will assume an ALL OPEN state unless their control is set to "fixed" and a closed Point-In-Time state. 











.. _custom Radiance materials: customRadianceMaterials.html


.. _Sky: sky.html


.. _Site Analysis: siteAnalysis.html 

.. _Radiation Map: radiationMap.html 

.. _Point-in-time Illuminance: illuminance.html

.. _Daylight Availability: daylightAvailability.html 

.. _Annual Glare: annualGlare.html

.. _Radiance Render: radianceRender.html

.. _Thermal Analysis: thermalAnalysis.html

.. _View Analysis: viewAnalysis.html


.. _Exterior Glass Shades: materials_exteriorGlass.html#shades-control-point-in-time-workflows

.. _Exterior Glass (Dynamic) Tint: materials_exteriorGlassDynamic.html#tint-state-point-in-time-workflows

.. _Exterior Glass Shades (annual): materials_exteriorGlass.html#shades-control-annual-workflows

.. _Exterior Glass (Dynamic) Tint (annual): materials_exteriorGlassDynamic.html#tint-state-annual-workflows