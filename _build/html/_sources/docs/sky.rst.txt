
Sky
================================================
.. figure:: images/Sky.jpg
   :width: 900px
   :align: center

The sky editor allows the specification of the sky luminance distribution for which a point-in-time illuminance simulation or scene rendering should be conducted. The sky can be set as follows:
	
	**Type:** The sky type sets the sky model being used such as the CIE clear, intermediate or overcast skies. For the Perez all weather sky direct and diffuse irradiance for the date and time selected are taken for the EPW weather files specified under `Location.`_
	
	**Month, Day and Hour:** Set the date and time of day for which the sky luminance distribution should be calculated.
	
	**Ground Albedo:** Sets the diffuse reflectance of the lower hemisphere in the scene. If a ray leaves the scene through the lower hemisphere without hitting an explicitly model ground object, this value is being used to estimate the luminance of the ground which will vary with prevailing sky condition.  A typical ground albedo is 20%. The user is encouraged to explicitly model any important nearby ground objects and to assign a specific material to these ground objects.
	
.. _Location.: Location.html