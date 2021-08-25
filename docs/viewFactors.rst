
View Factors
=========================
In the context of ClimateStudio's View Analysis workflow (see `setup instructions`_), view factors measure the percentage of view (by solid angle) occupied by a specific feature. The View Analysis workflow automatically calculates view factors for every layer and tag in the model, which can be visualized using the dropdown at the top of the View Factors tab:

.. _setup instructions: viewAnalysis.html

.. figure:: images/result_dashboardViewFactors.png
   :width: 900px
   :align: center

Selecting a layer or tag (in this case, the "Art" tag) reveals the corresponding view factors in the Rhino viewport:


.. figure:: images/result_viewportViewFactor.png
   :width: 900px
   :align: center

View factors for each location are computed using a field of view of 360 degrees horizontally, and 60 degrees vertically, centered on the horizon. The *subject* of a given pixel is taken to be the first opaque object that the view ray intersects, *or* the first object of any kind that the ray strikes *after* passing through vision glass (whichever comes first). In other words, view rays will pass through interior glass doors and partitions, but will stop when they encounter a glass facade across the street.

Below the feature dropdown and summary is the Room Table, which lists room-by-room view factors for all tags and layers in the model, and a Viewport Settings bar, which contains a legend and settings button (6) for adjusting the display:

.. figure:: images/result_panelViewFactorTable.png
   :width: 900px
   :align: center


















