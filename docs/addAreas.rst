
Add Areas
================================================
This subpanel is used to specify regularly occupied spaces within a building such a workareas, circulation spaces etc. Many standards and green building rating systems rely on the concept of “regularly occupied areas” to analyze the environmental performance of a building, such as daylighting, glare and thermal comfort, where it matters. In ClimateStudio regularly occupied areas are defined via reference surfaces. These surfaces are often coincident with the floor but may be objects on layers without any assigned material properties. To define a regularly occupied area left-click on the *Add Area* button and select one of more reference surfaces.  


.. figure:: images/AddAreas.jpg
   :width: 900px
   :align: center

In the example below, the two reference surfaces are coincident with the floor and marked in yellow. 

IMAGE

After selecting the surfaces and pressing *Enter* the *Edit Occupied Areas* panel opens. 

IMAGE

While occupied areas are continuous surfaces, lighting calculations conduct simulations at discrete sensor points that are distributed on a grid pattern across an occupied area and that are oriented along the surface normal areas. The *Edit Occipied Areas* panel includes the following customization settings:

	**ID:** Brief area description such as conference room or open office
	
	**Description:** Optional, more extensive description
	
	**Sensor Spacing:** Distance between sensors in model units
	
	**Sensor Inset:** Distance of sensors from the edge of the surface area. Some standards and lighting measurement specifications require a minimum sensor distance from walls and windows.
	
	**Workplane Offset:** Distance between the reference surface and the sensor plane. 
	
Once the occupied areas have been selected and specified, they appear in the Rhino Viewport and are added to a list in the *Add Areas* subpanel.The list provides statistics for each occupied area such as its area and number of sensors as well as the ability to edit or delete an area. A larger building may include hundreds of occupied areas. The *Tag* item therefore allows to organize areas by, for example, floor, program type and/or orientation. Once tagged, ares can be displayed selectively using the filter and tag functions above the table. 
	
IMAGE 
	