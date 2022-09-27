
Luminaires
================================================
ClimateStudio supports lighting calculations for daylit and electrically lit scenes. The daylight source is defined in the `Sky panel`_. For electric-lighting-only simulations, the sky can simply be set to nighttime. 

.. _Sky panel: sky.html

The Luminaires panel is used to select real-world luminaire products and place them in the Rhino model, either individually or in groups. To place a luminaire, left-click on the *Add Luminaire* button (**1**).

.. figure:: images/subPanel_luminaires.png
   :width: 900px
   :align: center
   
A dialog will appear, allowing the user to browse through a series of IES files (**2**) that come with ClimateStudio. 
An IES file is a manufacturer-supplied text file that provides the luminous intensity distribution of a lighting product on a spherical grid. 
This data is usually displayed three-dimensionally as a photometric web or in horizontal and vertical sections (**8**). 
Most lighting manufacturers provide IES files of their products on their websites. 
If you are experiencing difficulty locating an IES file for a specific product, try the `IES library`_. 

.. _IES library: https://ieslibrary.com/en/home

.. figure:: images/subPanel_selectLuminaire.png
   :width: 900px
   :align: center


Power Multiplier
<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
A linear multiplier (**3**) may be used to scale the luminous output of the fixture. This may be useful for setting ballast loss factors, etc.

Total Luminous Output
<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
The luminous output (**4**) is the total, spherically-integrated luminous flux emitted by the luminaire according to the IES file's photometric distribution. This quantity should not be confused with the product's rated lumen value, which may (or may not) be listed in the IES file header. The total flux accounts for interreflection losses within the fixture, and is a more reliable indicator of measured and simulated behavior than rated lumen values (when they exist).

Max Luminous Intensity
<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
The maximum intensity (**5**) is the luminaire's peak candela value. Both this field and the total luminous output scale with the power multiplier.

Lamp Color
<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<

Click on the RGB value (**6**) to change the luminaire's color. 


A dialog will appear with a drop-down (**10**) to switch between RGB color space and CCT, which generates a Planckian-locus color at the specified temperature. 
RGB colors are edited by clicking on the color box (**11**). 
CCT colors are set by typing a color temperature value or adjusting the slider (**12**). Color changes will affect the spectrum of the luminaire but not its luminous power.
Click *Update Luminaire Color* (**13**) to commit changes. 

.. figure:: images/subPanel_selectLuminaireColor.png
   :width: 900px
   :align: center


Lighting Zone
<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<

Luminaires can be assigned to a lighting zone (**7**). Lighting zones are collections of luminaires operated using the same control, such as an on/off or dimming switch. In ClimateStudio renderings, lighting zones are eligible for post-process brightness and color adjustment, as described `here`_. To assign a luminaire to a lighting zone, enter a zone name or choose an existing zone using the combo box. To make the zone eligible for post-process adjustments, check the Post-Process box (**18**) in the Luminaires Table (see next section).

.. _here: radianceRender.html#post-processing-of-lighting-zones

Once luminaire selection is complete, click the *Place in Rhino Model* button (**9**), 
which places the luminaire in the Rhino model at a user-specified point.
To create additional copies of the luminaire, simply use the *copy* or *array* commands in Rhino. 
Copying luminaires creates multiple instances of the same object (using block instances), 
allowing the entire set of instances to be edited in concert. 


Luminaires Table
<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<

.. figure:: images/subPanel_luminairesTable.png
   :width: 900px
   :align: center

The Luminaires Table lists all luminaire objects in the model and controls their display in the viewport. The checkbox in the table's far left column (**14**), along with the visibility of the luminaire blocks in Rhino, 
determines whether a luminaire is included in renderings and point-in-time illuminance calculations. 
**Only luminaires that are visible and enabled at the moment a simulation starts are included in the analysis.**

The *hWeb* (**15**) and *vWeb* (**16**) toggles control the visibility of the 3d photometric web preview, while the *webScale* (**17**) column controls its size. 

The *Post-Process* check box (**18**) determines whether a lighting zone is eligible for post-render adjustments, as described `here`_. Please note that all luminaires in a post-processed lighting zone will emit the same (adjustable) color. 

.. _here: radianceRender.html#post-processing-of-lighting-zones

In the scene above, eight instances of an ambient suspended fixture have been assigned to the perimeter zone of the open office space, and another eight to its interior zone. Six instances of a down light, meanwhile, have been placed in the small meeting room. 


