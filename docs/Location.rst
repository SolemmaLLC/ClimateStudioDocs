
Location
================================================
The location subpanel is used to specify the position of the site on earth by selecting the closest available typical meteorological year (TMY). 
A TMY file contains hourly measured data for a variety of physical quantities that are required for an environmental performance analysis, 
including direct and diffuse solar radiation, temperature and relative humidity levels as well as wind speed and direction.  

.. figure:: images/Location.jpg
   :width: 900px
   :align: center

**North Offset:** By default, North is along the positive y-axis. To adjust the North direction, use the slider or manually enter an angle.

**Show Compass:** Toggle to show the North arrow

**Display size:** Changes the relative size of the North arrow compared to other scene objects


The default site is the TMY3 file for Boston, Logan International Airport. 
To select another file, left-click on the file selector icon next to the name of the current TMY file. A `search dialog`_ should pop up. 


Climate File Formats
----------------------------------------------------
ClimateStudio uses the widely used `EnergyPlus weather file format`_ (file extension EPW). EPW files are available for thousands of sites worldwide and can be downloaded from the following websites. 

- `Department of Energy EPW files`_ 
- `Climate.OneBuilding.org`_ 

.. _EnergyPlus weather file format: https://energyplus.net/weather/simulation

.. _Department of Energy EPW files: https://energyplus.net/weather

.. _Climate.OneBuilding.org: http://climate.onebuilding.org/

.. _search dialog: searchWeather.html