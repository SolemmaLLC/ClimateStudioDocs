Double Slider Filters
================================================


.. figure:: images/filterSliderExample0.jpg
   :width: 900px
   :align: center


Double Sliders will select a range with a start value, an end value, and the range in between. 

There are currently 4 uses of the double slider filter: 

- **Days** of the year as a range (wraps around)
- **Hours** of the day as a range (wraps around)
- **Wind speed** as a range
- **Temperature** as a range


The **Days** and **Hours** filter allows "wraparounds" which means they allow start value > end value, where the range selected is everything >= the start value and everything <= the end value.

the **Wind Speed** filter's last number represents positive infinity. 


.. figure:: images/filterSliderExample1.jpg
   :width: 900px
   :align: center

In this example, we are filtering for data during **summer nights**. 


All four filters are applied to `Wind Rose`_, while only the **Days** and **Hours** filters are applied to `Psychrometric Chart`_. 
Moving the slider for **Days** and **Hours** filters will update the data displayed for both **Wind Rose** and **Psychrometric Chart**. 


.. _Wind Rose: windRose.html
.. _Psychrometric Chart: psychrometricChart.html
