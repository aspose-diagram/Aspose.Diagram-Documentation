---
title: Arbeiten mit Shapes Gluing
type: docs
weight: 10
url: /de/java/working-with-shapes-gluing/
---
## **Holen Sie sich die Steckverbinder in eine bestimmte Form geklebt**
[Visio Formen hinzufügen und verbinden](/diagram/de/java/add-and-connect-visio-shapes/) erklärt, wie man eine Form hinzufügt und sie mit anderen Formen in Microsoft Visio Diagrammen unter Verwendung von Aspose.Diagram for Java verbindet. Es ist auch möglich, Verbinder zu finden, die an diese Form geklebt sind.
### **Geklebte Formen erhalten**
 Die GluedShapes-Methode, die von der bereitgestellt wird[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)-Klasse kann verwendet werden, um eine Liste der IDs aller Konnektoren zu erhalten, die an eine Form geklebt sind, oder, wenn die betreffende Form eine Konnektor ist, die IDs der Formen, mit denen sie verbunden ist[ShapeCollection](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shapecollection) Klasse, kann dann verwendet werden, um eine Form anhand ihrer ID zu finden.

Der folgende Code zeigt, wie man:

1. Laden Sie eine Beispieldatei.
1. Greifen Sie auf eine bestimmte Form zu.
1. Rufen Sie eine Liste der IDs aller Verbindungsstücke ab, die an dieses Shape geklebt sind.
#### **Holen Sie sich Connectors Glued Programmierbeispiel**
Verwenden Sie den folgenden Code in Ihrer Java-Anwendung, um alle Verbinder zu finden, die mit Aspose.Diagram for Java an eine Form geklebt wurden.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetGluedConnectors.class);   
// call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "RetrieveShapeInfo.vsd");
// get shape by an ID
Shape shape = diagram.getPages().get(0).getShapes().getShape(90);
// get all glued 1D shapes
long[] gluedShapeIds = shape.gluedShapes(GluedShapesFlags.GLUED_SHAPES_ALL_1_D, null, null);

// display shape ID and name
for (long id : gluedShapeIds)
{
    shape = diagram.getPages().get(0).getShapes().getShape(id);
    System.out.println("ID: " + shape.getID() + "\t\t Name: " + shape.getName());
}

{{< /highlight >}}

## **Visio Formen mit Verbindungspunkt zusammenkleben**
Aspose.Diagram for Java ermöglicht es Entwicklern, Formen durch die Verbindungspunkte zusammenzukleben.
### **Formen kleben**
 Die GlueShapes-Methode, die von der bereitgestellt wird[Buchseite](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) Klasse verwendet werden kann.

|<p>**Geben Sie diagram ein** </p><p>![todo: Bild_alt_Text](http://i.imgur.com/Z69f4hg.png)</p>|<p>**Die diagram nach dem Kleben der Formen** </p><p>![todo: Bild_alt_Text](http://i.imgur.com/5TJpDwc.png)</p>|
|:- |:- |
Der folgende Code zeigt, wie man:

1. Laden Sie eine Beispieldatei.
1. Formen kleben.
1. Speichern Sie diagram.
#### **Glue Visio Formen Programmierbeispiel**
Verwenden Sie den folgenden Code in Ihrer Anwendung Java, um Formen durch die Verbindungspunkte zu kleben:


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GlueVisioShapes.class);
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get a particular page
Page page = diagram.getPages().getPage("Page-1");
// set shape id
long shape1_ID = 7;
long shape2_ID = 494;
// Glue shapes
page.glueShapes(shape1_ID, ConnectionPointPlace.CENTER, shape2_ID);

// Save diagram
diagram.save(dataDir + "GlueVisioShapes_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Kleben Sie Formen in den Behälter**
Aspose.Diagram for Java ermöglicht es Entwicklern, Gruppenformen in einen Container zu kleben.
### **Leimgruppenform**
Die GlueShapesInContainer-Methode, die von der Page-Klasse verfügbar gemacht wird, kann verwendet werden.

|<p>**Geben Sie diagram ein** </p><p>![todo: Bild_alt_Text](http://i.imgur.com/HRRzIEh.png)</p>|<p>**Die diagram nach dem Kleben der Gruppenformen** </p><p>![todo: Bild_alt_Text](http://i.imgur.com/YxCiOgU.png)</p>|
|:- |:- |
Der folgende Code zeigt, wie man:

1. Laden Sie eine Beispieldatei.
1. Gruppenformen kleben.
1. Speichern Sie diagram.
#### **Glue Shapes Inside Programmierbeispiel**
Verwenden Sie den folgenden Code in Ihrer Java-Anwendung, um die Gruppenform in einen Container zu kleben:


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GlueContainerShape.class);   
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get a particular page
Page page = diagram.getPages().getPage("Page-1");

// The ID of shape which is glue from Aspose.Diagram.Shape.
long shapeFromId = 779;
// The location on the first connection index where to glue
int shapeToBeginConnectionIndex = 72;
// The location on the end connection index where to glue
int shapeToEndConnectionIndex = 73;
// The ID of shape where to glue to Aspose.Diagram.Shape.
long shapeToId = 743;

// Glue shapes in container
page.glueShapesInContainer(shapeFromId, shapeToBeginConnectionIndex, shapeToEndConnectionIndex, shapeToId);

// Glue shapes in container using connection name
// page.GlueShapesInContainer(fasId, "U05L", "U05R", cabinetId1);

// Save diagram
diagram.save(dataDir + "GlueContainerShape_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

