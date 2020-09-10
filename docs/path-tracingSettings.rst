
Path-tracing Settings
================================================
.. figure:: images/IlluminanceSimulation.jpg
   :width: 900px
   :align: center
   
Under settings, the following parameters can be specified. For most simulations, these parameters can be left untouched.

**Sample Rays Per Sensor Per Pass:** The number of rays emitted for each sensor at each pass. Increasing this number may reduce the number of passes required before a simulation converges but also increases the time required for each pass.

**Maximum Number of Passes:** While the simulation can be stopped by the user at any moment by using the stop button, this parameter provides a hard stop for a simulation run. 

**Radiance Parameters:** By default, ClimateStudio considers up to 6 ambient bounces before discarding a ray. If you want to adjust these parameters,  you should familiarize yourself with the `Radiance rtrace parameter.`_ 

.. _Radiance rtrace parameter.: https://floyd.lbl.gov/radiance/man_html/rtrace.1.html

