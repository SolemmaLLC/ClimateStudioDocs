Revit Daylight Model Import 
-------------------------
This workflow imports a .cse file created by Climate Studio `Revit Exporter Plug-in`_ in order to run Daylight simulations with Climate Studio. 

.. _Revit Exporter Plug-in: revitExporter.html


Import .cse file from Revit
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
We recommend starting with an **Empty File**.

*[Insert Screen shot Workflow panel]*

Click button on workflow panel or Type Command `CSImportRevitCommand`. 

Select a .cse file to import. 

*[Insert Screen shot of Overwrite Existing Revit Objects Dialog, put numbers next to options]*

If this Rhino file contains Rhino Objects with RevitElementID attached, this dialog will pop up to ask if you want to overwrite the existing import. 

1. Selecting **Overwrite** will Delete all Rhino Objects with Revit ElementIDs attached as a user-dictionary. It will remember the Rhino Layer each Revit Element is placed in. Later, the plug-in will place newly imported Revit Element with the same ID into the remembered Rhino Layer. 
2. Selecting **Keep** will keep current Rhino Objects and Import the new model. 

*[Insert Screen shot of Importing Model]*

**Window** Geometries are reduced to **single plane geometry**. Windows are separated into “interior” or “exterior” layers depending on the host wall and Rooms information provided in the Revit model. Exterior windows have normals facing outside. 

**Rooms** from Revit are used to define **Occupied Areas** which can be turned into **Simulation Grids**. The names and IDs of the grids will be populated with the respective Room name and Room ID. 

Default LM84 simulation materials are selected in the `Materials`_ Panel.


*[Insert Screen shot of Layer table after import with example sub-layer organizations]*

Elements from Revit are placed into different Rhino layers depending on their **Demolished Phases, Design Option, Category, and Family Type.** 

We especially recommend `checking your model`_ if Rooms are Not Imported, multiple phases exist in this model, there are complex window geometries, or you are overwriting the current model. This page also contains some tips on organizing imported geometries. 

.. _checking your model: revitImportTroubleShoot.html


Set up Daylight Simulation
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

*[Insert Screen shot of Materials Panel after Import]*

In the `Materials`_ panel Default LM83 materials are assigned on Import (to a fresh Rhino file). 

*[Insert Screen shot of Occupied Areas Panel after Creating Occupied Areas]*

Populate the `Occupied Areas`_ panel with surfaces from Rhino Layer "Occupied Areas", the ID and Name of each grid will be auto-assigned based on the Room ID and Room Name in Revit.  

The Imported Revit Model can be used to run the following analysis:

| `Daylight Availability`_
| `Annual Glare`_
| `Radiance Render`_
| `Radiation Map`_
| `View Analysis`_

.. _Daylight Availability: daylightAvailability.html
.. _Annual Glare: annualGlare.html
.. _Radiance Render: radianceRender.html
.. _Radiation Map: radiationMap.html
.. _View Analysis: viewAnalysis.html

.. _Materials: materials.html
.. _Occupied Areas: occupiedAreas.html


Combining Multiple Revit Models
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
We Recommend Import each Revit model in their own Rhino file, make changes to layer organization as needed, then combine the Rhino Files. This way, when re-importing (overwriting) each Revit file to their own Rhino file, the manual layer organization will be remembered. 

Alternatively you may Import another .cse file and select **Keep Current Model** when asked. The combined Rhino file CANNOT run a overwrite import as multiple Rhino Objects are attached with the same Revit Element IDs. 