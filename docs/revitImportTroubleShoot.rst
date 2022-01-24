Revit Import Trouble Shoot
-------------------------

Checking Exported Model
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
- Each layer in Rhino will be assigned a material, so make sure geometries in the same layer have the same material. Move them into different layers or create new layers if needed. These changes are remembered when running a overwrite import. 
- Check all glazing geometry are single plane meshes. 
- Check all exterior windows are on the exterior window layer. 
- Check all exterior windows with blinds have normals that point outside. 
- Check all occupied areas have normals that point up. 

Tips on Filtering Objects in Rhino
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

*[Insert Screen shot of properties panel showing user text and right click on panel to highlight Select by Key and Value]*

Rhino Objects are tagged with **Attribute User Text** based on data exported from Revit. It may include the following tags: 

- **RevitType** - the Revit Family name appended with Revit Type name
- **RevitName**
- **RevitElementID** - used to identify objects on overwrite import
- **DesignOption**
- **Category** - the Revit Category
- **Normal**
- **Level** - the Revit Level this objects is in
- **CreatePhase**
- **DemolishPhase**
- **Glazing** - set by the revitImporter depending on the opacity of the material
- **Exterior** - a tag if the object it self is a Wall with "Exterior Wall Type" or the object is hosted by a "Exterior Wall Type" wall
- **Room**
- **HostID**
- **HostName**
- **HostCategory**
- **RoomArea** - room area in sqft
- **GeometryIndex** - used to identify objects on overwrite import when one Revit Element is imported as multiple Rhino Objects

Right click on the **Attribute User Text** Panel in Rhino to select objects with the same Key and Value tagged. 

This is a good way to filter objects for reorganization. For example: select objects created in the same phase or objects on the same level. 

Cleaning Exported Model
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

*[Insert Screen shot layer table and rhino viewport after running Import Demolished Geometries Command]*

3D windows and Rooms are not baked into Rhino on import by default, as only their single-plane representations are needed for daylight simulations. 

The **CSImportRevitDiscardedGeometries** command will import those 3D Windows and Rooms. This can be used if single plane windows or occupied areas are not created correctly. 
