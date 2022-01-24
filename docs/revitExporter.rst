Revit Export Daylight Model
-------------------------
This workflow exports Revit model elements to a .cse file for `Climate Studio Rhino to import`_ a Daylighting model. 

Revit **ElementID**, **Category**, **Family Type**, **Design Option**, and **Phases** data are attached to each element. This information will be used to organize geometries into layers on Rhino Import. 


.. _Climate Studio Rhino to import: revitImporter.html

Export Revit Model
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Open Revit model

*[Insert Screen shot of Revit Tool Bar, put 1 next to "Climate Studio" tab and 2 "Export Daylighting Model" button]*

Navigate to (1) **Climate Studio** tab, and click on (2) **Export Daylight Model**

*[Insert Screen shot of View Filter Selection Window, put 1 next to "Export Entire Model" and 2 next to "Export Visible"]*

1. **Export Entire Model** exports all 3D model elements in this model


2. **Export Visible** will export all elements that are visible in the current active view. We recommend having a **3D View** as your current active view with a **Section Box**. While the Section Box cuts geometries intersecting the edge of selection, the exporter will export the entire geometry. 

click **OK** and the Categories table will show up. 



*[Insert Screen shot of Categories table, put numbers next to each button, collage with screen shot of Layers table]*

The **Categories table** is a list of all the categories present in this model, which shows the number of elements each category contains. A set of default categories to export are already selected, make modifications if needed. 

1. Click on **...** to see which Family Types exist in each Category. 


2. Check the **Expand Type option** for each Family Type to have their own Rhino sub-layers for assigning different materials.


3. By default, All Rooms elements that are “Placed” are exported. **Rooms** are used to created Occupied Areas as simulation grids. Additionally, this information is required for distinguishing exterior windows from interior windows, and to correctly set the normals of exterior windows. 


4. By default, Geometries with “Demolished Phase” will NOT be exported. Check **Export Demolished Geometries** to export them. Exporting demolished geometries might result in overlapping geometries in the Rhino model that requires manual clean-up. 


5. Click **OK** to export into .cse file. 

*[Insert Screen shot of export loading bar]*

Elements are exporting. When completed, select Location to save the exported .cse file. 

`Import .cse file to Climate Studio Rhino.`_

.. _Import .cse file to Climate Studio Rhino.: revitImporter.html
