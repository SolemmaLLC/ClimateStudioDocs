Revit Export Daylight Model
-------------------------
This workflow exports Revit model elements to a .cse file for `Climate Studio Rhino to import`_ a Daylighting model. 

Revit **ElementID**, **Category**, **Family Type**, **Design Option**, and **Phases** data are attached to each element. This information will be used to organize geometries into layers on Rhino Import. 


.. _Climate Studio Rhino to import: revitImporter.html

Export Revit Model
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Open Revit model

.. figure:: images/revit_toolbar.png
   :width: 900px
   :align: center
   
Navigate to (1) **Climate Studio** tab, and click on (2) **Export Daylight Model**

.. figure:: images/revit_viewfilter.png
   :width: 900px
   :align: center

| 3 - **Export Entire Model** exports all 3D model elements in this model


| 4 - **Export Visible** will export all elements that are visible in the current active view. We recommend having a **3D View** as your current active view with a **Section Box**. While the Section Box cuts geometries intersecting the edge of selection, the exporter will export the entire geometry. 

click **OK** and the Categories table will show up. 



.. figure:: images/revit_categoriestable.png
   :width: 900px
   :align: center

The **Categories table** is a list of all the categories present in this model, which shows the number of elements (5) and sub-family-types (7) each category contains. A set of default categories to export are already selected, make modifications if needed. 

Click on **...** (8) to see which Family Types (9) exist in each Category. Check **Expand Type** (6) for each Family Type to export to their own Rhino sub-layers for assigning different materials.

By default, All Rooms elements that are “Placed” are exported (10). **Rooms** are used to created Occupied Areas as simulation grids. Additionally, this information is required for distinguishing exterior windows from interior windows, and to correctly set the normals of exterior windows. 

By default, Geometries with “Demolished Phase” will NOT be exported (11). Check **Export Demolished Geometries** to export them. Exporting demolished geometries might result in overlapping geometries in the Rhino model that requires manual clean-up. 

Click **OK** to export .cse file. 

.. figure:: images/revit_exporting.png
   :width: 900px
   :align: center

Elements are exporting. When completed, select Location to save the exported .cse file. 

`Import .cse file to Climate Studio Rhino.`_

.. _Import .cse file to Climate Studio Rhino.: revitImporter.html
