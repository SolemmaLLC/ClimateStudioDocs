Custom Radiance Material
================================================
ClimateStudio lets you import custom Radiance materials using .rad files or BSDF .xml files. Please note that you need to be familiar with the `Radiance material modifiers`_ to use this option. 

.. figure:: images/matBrowser_custom.png
   :width: 900px
   :align: center

|
Use the **Manage button (3)** to create a new library. A pop-up dialog will guide you through the process (see below). Use the **Library dropdown (1)** to switch between existing libraries, and the **Reload button (2)** to refresh the current library (e.g. if the .rad files in its source directory have changed). 

Imported materials for the currently-selected library are shown in the **Material table (5)**. A text area at the top of the dialog shows the Radiance definition for the currently selected material. A rendered preview is currently supported only for *plastic*, *metal*, or *glass* materials without texture modifiers.

Defining a Custom Library
----------------------------------------------------

Step 1: Create a Library Directory
	Create a directory in which you want to store your custom Radiance materials, e.g. ``Documents\RadianceMaterials``.  

Step 2: Create Radiance Material File(s)
	Create one or more Radiance materials and add them to the directory. Each material definition should be saved as its own .rad file, and should include any modifiers referenced by the definition. An example file for a bright red material can be downloaded `here.`_ 	

Step 3: Link the Material Library to ClimateStudio
	Click on the manage button (**3**) to open the custom library manager: 
	

   .. figure:: images/matBrowser_custom_add.png
      :width: 900px
      :align: left

   Use the **Add button (6)** to add a library directory, or the **Remove button (7)** to remove an existing folder. The list of currently-loaded libraries is shown in the table (**8**). These will be the options available in the library dropdown (**1**). 

Step 4: Select Your Custom Library and Assign a Material
   Exit the library manager and select your library using the library dropdown (**1**). Use the material table (**5**) to select a material, and click the *Select* button to make the assignment.

.. _Radiance material modifiers: https://www.radiance-online.org/learning/documentation
.. _here.: https://climatestudiodocs.com/ExampleFiles/BrightRed.rad
.. _materials: materials.html

|
Back to `Materials`_.

.. _annual workflows: materials.html#dynamic-materials

.. _point-in-time workflows: materials.html#dynamic-materials

.. _Materials: materials.html

.. _Daylight Availability: daylightAvailability.html

.. _Annual Glare: annualGlare.html

.. _occupied area's property panel: occupiedAreas.html

.. _above: materials_exteriorGlass.html#shade-control-point-in-time-workflows