Results Comparison
-------------------------
The Results Comparison tool is a graphical interface for comparing multiple `thermal analysis`_ results. It features a stacked bar graph that can be used to track the energy performance of a set of design variants vis-a-vis baselines and targets. The window can be launched from a button at the top of the `results panel`_.

.. _thermal analysis: thermalAnalysis.html
.. _results panel: results.html

.. figure:: images/compareInput.jpg
   :width: 900px
   :align: center
   
To load results for comparison, either pre-select files in the results panel table prior to launching the window, or load files directly using the *Select Results* browser in the window's upper left corner:
   
.. figure:: images/selectResults.jpg
   :width: 150px
   :align: center


The browser includes buttons for adding, removing, or reordering files in the list. (Reordering is also possible by dragging and dropping items within the bar graph.) You may also save the current comparison, or reopen a previously saved comparison file.

Various metrics can be plotted in the bar graph, which are set using the *Graph Settings* panel. Available options include Energy Use Intensity (EUI), Carbon, Cost, and Energy Flows, which include all heat gains and losses. Metrics may be displayed using absolute or area-normalized values.

.. figure:: images/DataToGraph.jpg
   :width: 150px
   :align: center


Below the bar graph is a table that recapitulates the output values in the graph, followed by a comprehensive list of model input parameters. The input parameters provide a numerical record of changes made from one design option to the next. To highlight these distinctions, small triangles are drawn in each cell to indicate increases or decreases vis-a-vis the baseline (left-most) option.

Both the graph and the table can be exported in PNG or PDF format. The table can also be copied as a CSV file. 

.. figure:: images/exporttablepdf.jpg
   :width: 600px
   :align: center