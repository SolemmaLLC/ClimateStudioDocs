
LEED Daylight Option 1
================================================
Leadership in Energy and Environmental Design (`LEED`_) is a green building rating system maintained by US Green Building Council (`USGBC`_). The system offers two simulation-based options for achieving its Daylight Credit. Option 1, described here, simulates daylight availability throughout the entire year, while `Option 2`_ simulates daylight availability at two specific moments in time. Option 1 yields a more complete description of daylighting performance, offers more potential points under the USGBC's rating system, and is the recommended compliance pathway for the LEED Daylight Credit.

.. _LEED: https://www.usgbc.org/leed
.. _USGBC: https://www.usgbc.org/
.. _Option 2: daylightLEEDOpt2.html

Upon completion of the first simulation pass (`setup instructions here`_), or upon loading a saved `result`_, the results panel will show a dashboard with five key metrics:

.. _setup instructions here: daylightAvailability.html
.. _result: results.html

.. figure:: images/result_dashboardLEEDOpt1.png
   :width: 900px
   :align: center

1. **Credits**: The number of points the building qualifies for. Points are based on the total spatial daylight autonomy (sDA) of all qualifying areas. Areas that receive too much direct sunlight (ASE) are automatically disqualified from the total under LEED version 4.0, though not under version 4.1. In the latter case, please note that ASE values above 10% must be justified in writing as part of the submitted report. 
   
.. figure:: images/LEEDcredits.png
   :width: 900px
   :align: center


2. **Spatial Daylight Autonomy (sDA)**: The percentage of the regularly occupied floor area that is "daylit." In this context, "daylit" locations are those meeting target illuminance levels (300 lux) using daylight alone for at least 50% of occupied hours. Such locations are said to be 50% *daylight autonomous*. sDA calculations are based on annual, climate-based simulations of thousands of different sky conditions throughout the year. Per LM-83 guidelines, dynamic shading devices such as blinds or electrochromic glazings **must** be specified for all exterior window units.

.. figure:: images/result_viewportSDA.png
   :width: 900px
   :align: center

3. **Annual Sunlight Exposure (ASE)**: The percentage of the regularly occupied floor area that is "overlit." In this context, "overlit" locations are those receiving direct sunlight (>1000 lux directly from the solar disc)  for more than 250 occupied hours. LEED versions 4.0 and 4.1 differ in how strictly ASE limits are enforced. It is worth pointing out that ASE is calculated for the dynamic shading system fully opened all year, whereas sDA takes the operation of dynamic shading into account. This distinction can cause confusion, but is meant to encourage passive solar design strategies. 

.. figure:: images/result_viewportASE.png
   :width: 900px
   :align: center

4. **Mean Illuminance**: The average illuminance over the regularly occupied floor area over all occupied hours. Selecting the metric in the dashboard enables perusal of both mean and hourly illuminance data in the Rhino viewport.
 
.. figure:: images/result_viewportIllum.png
   :width: 900px
   :align: center
   
5. **Blinds Open**: The average percentage of dynamic window area that is *unshaded* during occupied hours. This metric is an important indication of the frequency of blinds use in response to direct solar exposure. Lower numbers here indicate higher rates of blinds use, which correspond to lower daylight levels and reduced views to the outside. As with ASE, blinds operation can be minimized through passive design strategies such as orientation, static shading, and reduced window-to-wall ratio.

Results panel
--------------------------

.. figure:: images/result_panelLEEDOpt1.png
   :width: 900px
   :align: center

The LEED Option 1 results panel has five sections:

- The **Header** ...

- The **Building Dashboard** ...




Reporting
-----------
A key ClimateStudio feature is the ability to create automated simulation results in PDF file format. To generate a report, select the PDF icon to the far right of the simulation result. 

.. figure:: images/daylightAvailability5.png
   :width: 900px
   :align: center

The report generator allows you to customize your report by adding your company logo. In the case of LEED v4 reporting, you can also provide a reason for ASE exceedance, if applicable. See the LEEDv4 technical menu for details. 

.. figure:: images/daylightAvailability6.png
   :width: 400px
   :align: center

An example report can be `downloaded here`_. As of summer 2020, the US Green Building Council accepted ClimateStudio reports for compliance for LEEDv4 Daylighting Credit option 1. 
Follow the procedure below during submission. The LEED Online form will soon be updated to allow for this option.


	**Add this language to the “Special Circumstances” section of the LEED Online credit form**: 

	Thank you for your request for approval of the Solemma ClimateStudio daylight simulation report for LEED EQ credit: Daylight documentation. The ClimateStudio report may be used in lieu of the Daylight and Quality Views Calculator documentation requirements outlined in the LEED Online credit form.  The report or supporting documentation must include daylight details for all regularly occupied spaces in the project. 

	GBCI reviewer questions may be directed to Larissa Oaks at USGBC (loaks@usgbc.org)

	

.. _downloaded here: https://climatestudiodocs.com/ExampleFiles/SampleProject_LEEDv4.1_Daylighting_Report.pdf

































