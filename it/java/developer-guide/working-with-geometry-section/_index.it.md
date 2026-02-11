---
title: Lavorare con la sezione Geometria
type: docs
weight: 180
url: /it/java/working-with-geometry-section/
---
## **Modifica la sezione geometrica di una forma connettore**
Qualsiasi forma in Microsoft Office Visio è composta da una o più "geometrie". Ogni geometria rappresenta un diverso componente della forma. La maggior parte delle forme ha una sola geometria, ma alcune ne hanno due o più. Le API Aspose.Diagram consentono agli sviluppatori di gestire queste geometrie in modo programmatico.

I frammenti di codice seguenti gestiscono le geometrie di una forma.
### **Esempio di programmazione**
I frammenti di codice seguenti gestiscono le geometrie di una forma.


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

