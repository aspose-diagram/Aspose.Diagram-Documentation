---
title: Working with Geometry Section
type: docs
weight: 180
url: /java/working-with-geometry-section/
---

## **Modify Geometry Section of a Connector Shape**
Any shape in Microsoft Office Visio is composed of one or more “geometries.” Each geometry represents a different component of the shape. Most shapes have just one geometry, but some have two or more. Aspose.Diagram APIs allow developers to manage these geometries programmatically.

The code snippets below manage geometries of a Shape.
### **Programming Sample**
The code snippets below manage geometries of a Shape.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(EditConnectorGeometry.class);    
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

//set connector shape id
long connectorId = 4;
Shape connector = diagram.getPages().getPage("Page-1").getShapes().getShape(connectorId);
//get connector geometry at index 0
LineTo defaultLineTo = connector.getGeoms().get(0).getCoordinateCol().getLineToCol().get(0);
//remove connector geometry from index 0
connector.getGeoms().get(0).getCoordinateCol().getLineToCol().get(0).setDel(BOOL.TRUE);

//initialize LineTo geometry object
LineTo lineTo = new LineTo();
//set X value
lineTo.getX().setValue(0);
//set Y value
lineTo.getY().setValue(defaultLineTo.getY().getValue() / 2);
//add connector geometry
connector.getGeoms().get(0).getCoordinateCol().add(lineTo);

//initialize LineTo geometry object
lineTo = new LineTo();
//set Y value
lineTo.getY().setValue(defaultLineTo.getY().getValue() / 2);
//set X value
lineTo.getX().setValue(defaultLineTo.getX().getValue());
//add connector geometry
connector.getGeoms().get(0).getCoordinateCol().add(lineTo);

//initialize LineTo geometry object
lineTo = new LineTo();
//set X value
lineTo.getX().setValue(defaultLineTo.getX().getValue());
//set Y value
lineTo.getY().setValue(defaultLineTo.getY().getValue());
//add connector geometry
connector.getGeoms().get(0).getCoordinateCol().add(lineTo);

//save diagram in VDX format
diagram.save(dataDir + "EditConnectorGeometry_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

