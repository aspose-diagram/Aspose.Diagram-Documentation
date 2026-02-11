---
title: Arbeiten mit dem Geometrieabschnitt
type: docs
weight: 180
url: /de/java/working-with-geometry-section/
---
## **Ändern Sie den Geometrieabschnitt einer Verbindungsform**
Jede Form in Microsoft Office Visio besteht aus einer oder mehreren „Geometrien“. Jede Geometrie repräsentiert eine andere Komponente der Form. Die meisten Formen haben nur eine Geometrie, aber einige haben zwei oder mehr. Aspose.Diagram APIs ermöglichen Entwicklern, diese Geometrien programmgesteuert zu verwalten.

Die folgenden Codeausschnitte verwalten Geometrien einer Form.
### **Programmierbeispiel**
Die folgenden Codeausschnitte verwalten Geometrien einer Form.


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

