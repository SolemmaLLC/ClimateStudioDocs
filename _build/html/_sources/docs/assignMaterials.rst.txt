
Assign Materials
================================================
Each object in the Rhino scene is located on a single layer. ClimateStudio uses these layers to assign material properties to scene objects. Material on layers without an assigned material are ignored by all lighting simulations. 

.. figure:: images/AssignMaterials.jpg
   :width: 900px
   :align: center

To assign a material to a layer, double-click on the material row next to the layer and Edit Layer Material panels will appear. ClimateStudio comes with an extensive library of measured materials which are divided into opaque, transparent and translucent elements. The top part of the Edit Layer Material panels shows a visualization of the currently selected material along with its Radiance material modifier to the right. The filter at the bottom allow to search the material database by material type or certain properties such as total visual reflectance (Rvis(total)). Expert users may also link `custom radiance materials.`_ 

.. _custom radiance materials.: customRadianceMaterials.html

.. figure:: images/WhiteCeilingPanels.jpg
   :width: 900px
   :align: center

