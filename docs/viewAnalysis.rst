
View Analysis
================================================
This workflow assesses occupant views and computes eligibility for the LEED v4 Quality Views credit (and, as of ClimateStudio v1.5, the EN 17037 European standard). It can also be used to calculate view factors and view distances to specific model layers or objects of interest.

Simulation Setup
--------------------

.. figure:: images/workflowPanel_view.png
   :width: 900px
   :align: center

|

To prepare a model for simulation, work your way though the materials and occupied-areas subpanels, labeled 1 and 2 in the figure above. You may also import tree assets, which are pre-tagged as *Nature/Vegetation* layers.

| 1 - `Materials`_
| 2 - `Occupied Areas`_ 
| 3 - `Scene Assets`_ (optional): `Trees`_ (5)
| 4 - `Import .cse file from Revit`_ (optional)

.. _Materials: materials.html

.. _Occupied Areas: occupiedAreas.html

.. _Import .cse file from Revit: revitImporter.html

.. _Trees: tree.html

.. _Scene Assets: sceneObjects.html

When assigning materials, a **VisionGlass** tag must be attached to layers that represent exterior vision glazing. Although the materials specified in the Material column determine the optical behavior of surfaces in the model (and hence what can be seen from any vantage), a separate View Tag is required to distinguish the "vision glazing," because it is specifically through these surfaces that views and view distances are measured. Please note that **layers not given a material (left column) will not be included in the simulation**.
 
.. figure:: images/result_viewSetup.png
   :width: 900px
   :align: center

If you are submitting for LEED certification, you may also wish to organize and tag model layers containing features of visual interest, including *Nature/Vegetation*, streetscapes busy with *Movement* (LEED v4.0), and *Art* or *Urban Landmarks* (LEED v4.1). If you are testing for EN 17037 compliance, the only tag of relevance (other than *VisionGlass*) is the *Ground* tag.

If you have not done any lighting simulations in ClimateStudio, it is recommended that you initially go through the `Lighting Model Setup`_ video tutorial (5 minutes). The Rhino file used in the tutorial is available for `download`_.

.. _Lighting Model Setup: https://vimeo.com/392379928 
.. _download: https://climatestudiodocs.com/ExampleFiles/CS_Two_Zone_Office.3dm
 

Once all required inputs have been populated, a simulation is invoked by pressing the start button (6). The number of CPU cores used can be adjusted via the settings dialog (7).
 
Simulation Results
--------------------
The View Analysis workflow performs multiple types of view assessment. When the calculation is finished, or when a saved result is loaded, the `results panel`_ will show a summary with three tabs. Use the links below to skip ahead to the option of interest.

.. _results panel: results.html

.. figure:: images/result_viewTabs.png
   :width: 900px
   :align: center

.. toctree::
   :maxdepth: 1
   
   LEED<viewLEED.rst>
   EN 17037<viewEN17037.rst>
   View Factors<viewFactors.rst>




























