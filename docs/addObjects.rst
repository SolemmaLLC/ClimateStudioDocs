
Add Objects
================================================
.. figure:: images/AddObjects.jpg
   :width: 900px
   :align: center

This subpanel is used to build up a multi-zone EnergyPlus model. ClimatStudio supports the following geometric objects: Zones, Windows, Adiabatic/Ground and Shading. 

.. figure:: images/addObjects.png
   :width: 200px
   :align: center

Thermal Zones
----------------
Thermal zones are modeled as closed breps in Rhino. Thermal zones are the fundamental building blocks of thermal simulation programs. They consist of areas within a building that are conditioned to the same temperature, have the same programmatic use (such as office or classroom) and experience comparable loads from solar radiation etc. A thermal zone is not necessarily the same as a room. A row of identical, south facing classrooms can be treated as a single zone since there will be no heat flow between the classrooms if they are used in the same way. On the other hand, a large open office area should be divided into perimeter zones bordering the building envelope with a depth of around 5m (15 feet)  and a core zone (see below). Combining core and perimeter zones in a single zone leads to an underprediction of conditioning loads since a surplus of solar gains in an equator facing zones is credited to heating required on the non equator-facing side whereas in reality local cooling and heating may be required at the same time. 

.. figure:: images/addObjects2.png
   :width: 600px
   :align: center

Spaces on different floors should also not be combined into a single zone because ClimateStudio identifies downward facing surfaces as floors and assigns internal loads for equipment and occupants by floor area. Combining two floors into a single zone thus halves those loads.  

The figure below shows an example zoning model of a two story wing with bands of classrooms boarding a central circulation area. The whole wing should me modeled as six zones with north and south facing classroom on both floors and a core zone for the aisle.  

.. figure:: images/addObjects3.png
   :width: 900px
   :align: center

Neighboring zones have to be modeled carefully so that their surfaces actually touch so that EnergyPlus understands that the overlapping surface area between them is interior.

Once one or several breps have been selected as thermal zones, the user should press enter and the Zone dialogue appears.

IMAGE

ClimateStudio comes with a large election of predefined thermal zone descriptions including the USE Department of Energy (DOE) Commercial `Prototype Building models.`_ These preset zone templates are descriptions of typical commercial US buildings located in different ASHRAE climate zones. For example, BOston is located in climate zone 5A. By using the filter function in the Zone dialogue the user can , for example, all benchmark building types available in the ClimateStudio database such as Midrise Apartment, Medium Office and Strip Mall.  

.. _Prototype Building models.: https://www.energy.gov/eere/slsc/building-energy-use-benchmarking

IMAGE

Windows
-----------
Any type of envelope opening such as windows or skylights are models as flat surfaces with three or four corner points.Window surfaces have to be completely embedded in a zone surface to be recognized as a child object of a zone wall or roof. 

Note: 
	While window surfaces in EnergyPlus may not touch the edge of a zone surface, you may draw a window in CLimateStudio by just snapping at the corner points of a wall. ClimateStudio will then slightly offset the corner of the window for the wall surface.     

Shading
--------------
Shading surfaces may represent an overhang or parts of a neighboring building that shade thermal zone or window objects. EnergyPlus will create a shading mask for each window and all shading surfaces. This process is both slow as well as somewhat unstable so it is recommended that shading surfaces are assigned somewhat selectively. For example, in the urban massing model below shading surfaces are the overhangs as well as walls from neighboring buildings facing the apartment building in the center. 

IMAGE
