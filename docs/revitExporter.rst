Revit Export Daylight Model
-------------------------
This workflow exports Revit model elements to a .cse file for `importing a Climate Studio Daylight model in Rhino`_. 

.. _importing a Climate Studio Daylight model in Rhino: revitImporter.html


The exporter attaches Revit **ElementID**, **Category**, **Family Type**, **Design Option**, and **Phases** data to the geometries. This information will be used to organize geometries into Rhino layers on Import. 

Currently the Revit Export workflow is still in Beta release, please email us if you run into any issues. This feature is only available in Climate Studio v1.7 or newer.  


Export Revit Model
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Open Revit model. 

.. figure:: images/revit_toolbar.png
   :width: 900px
   :align: center
   
| 1,2 - Navigate to **Climate Studio** (1) tab -> click on **Export Daylight Model** (2). 

.. figure:: images/revit_viewfilter.png
   :width: 900px
   :align: center

| 3 - **Export Entire Model** exports all 3D model elements in this model

| 4 - **Export Visible** exports all visible elements in the active view. Use a **3D View** as your current active view and a **Section Box** to filter out elements. The Section Box cuts geometries intersecting the edge of selection, the exporter will export the entire geometry.  

click **OK** and the Categories table will show up. 

.. figure:: images/revit_categoriestable.png
   :width: 900px
   :align: center

The **Categories table** is a list of all the categories present in this model. A set of default categories to export are already selected. 

| 5 - **Element Count:** The number of elements each category contains gives a hint to which categories are essential.  

| 6 - **Explode Types:** Check for each Family Type to export as individual Rhino sub-layers if types require different materials.  

| 7 - **Type Count:** Number of Family Types in this category.    

| 8 - **See Types:** Click on **...** to see Family Types of this category.  

| 9 - **Types Table:** Show list of Family Types.  

| 10 - **Export Rooms:** All Rooms elements that are “Placed” are exported by default. **Rooms** are used to created **Occupied Areas** as simulation grids. Additionally, this information is required for distinguishing exterior windows from interior windows, and to correctly set the normals of exterior windows. Only un-check this if the rooms information is unreliable.  

| 11 - **Export Demolished:** Geometries with “Demolished Phase” will NOT be exported by default. Check **Export Demolished Geometries** to export them. Exporting demolished geometries might result in overlapping geometries in the Rhino model that requires manual clean-up.  

Click **OK** to export .cse file. 

.. figure:: images/revit_exporting.png
   :width: 900px
   :align: center

Elements are exporting. When completed, select Location to save .cse file. 

`Import .cse file to Climate Studio Rhino.`_

.. _Import .cse file to Climate Studio Rhino.: revitImporter.html
