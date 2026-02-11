---
title: Drehen, ändern Sie die Position und verbinden Sie Unterformen
type: docs
weight: 60
url: /de/java/rotate-change-the-position-and-connect-sub-shapes/
---
## **Drehen Sie eine Form mit einem geeigneten Winkel**
 Mit Aspose.Diagram for Java können Sie eine Form in einen beliebigen Winkel drehen. Die SetAngle-Methode, die von der bereitgestellt wird[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) -Klasse kann verwendet werden, um eine Form in jeden gewünschten Winkel zu drehen. Es nimmt einen einzelnen Parameter als Winkel an.
### **Drehen eines Formprogrammierungsbeispiels**
Verwenden Sie den folgenden Code in Ihrer Java-Anwendung, um eine Form mit Aspose.Diagram for Java zu drehen.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RotateVisioShape.class); 
// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-3");
// get shape by id
Shape shape = page.getShapes().getShape(16);

// Add a shape and set the angle
shape.setAngle(190);

// Save diagram
diagram.save(dataDir + "RotateVisioShape_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Ändern Sie die Position einer Form**
Mit der Shape-Klasse können Sie die Position einer Form ändern. Die Verbindungslinie passt sich automatisch an, wenn die Form an eine andere Position verschoben wird.

Die Move- und MoveTo-Methoden, die von der Shape-Klasse verfügbar gemacht werden, unterstützen das Ändern der Position einer Form als Teil einer Gruppe oder nicht.
Die Codebeispiele in diesem Artikel verschieben eine Form auf der Seite.
**Geben Sie diagram ein** 

![todo: Bild_alt_Text](http://i.imgur.com/cThgWnB.png)


**Die diagram, nachdem die Form verschoben wurde** 

![todo: Bild_alt_Text](http://i.imgur.com/Q3QByqe.png)

Der Vorgang zum Verschieben einer Form ist:

1. Laden Sie eine diagram.
1. Finden Sie eine bestimmte Form.
1. Verschieben Sie die Form an einen anderen Ort
1. Speichern Sie die diagram.
### **Beispiel für die Programmierung der Position ändern**
Das folgende Code-Snippet zeigt, wie die Form verschoben wird. Der Code ruft eine Visio-Seite nach Name und Form nach ID 16 ab und verschiebt ihre Position.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(MoveVisioShape.class);  
// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-3");
// get shape by id
Shape shape = page.getShapes().getShape(16);
// move shape from its position, it adds values in coordinates
shape.move(1, 1);

// save diagram
diagram.save(dataDir + "MoveVisioShape_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Verbinden Sie Unterformen der Gruppen**
In diesem Thema wird erläutert, wie zwei Unterformen von zwei verschiedenen Gruppenformen in Microsoft Visio-Diagrammen mithilfe von Aspose.Diagram for Java verbunden werden.

 Die ConnectShapesViaConnector-Methode, die von der bereitgestellt wird[Buchseite](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) Klasse kann verwendet werden, um die Shapes über ihre IDs zu verbinden. Die AddShape-Methode, verfügbar gemacht durch die[Diagram](https://reference.aspose.com/diagram/java)Klasse, kann verwendet werden, um eine Form hinzuzufügen.

|<p>**Die Eingabe diagram** </p><p>![todo: Bild_alt_Text](http://i.imgur.com/74rDby5.png)</p>|<p>**Die diagram nach der Verbindung von Unterformen** </p><p>![todo: Bild_alt_Text](http://i.imgur.com/c387dZJ.png)</p>|
|:- |:- |
Der folgende Code zeigt, wie man:

1. Laden Sie eine Beispieldatei.
1. Greifen Sie auf eine bestimmte Seite zu.
1. Fügen Sie der ausgewählten Seite eine dynamische Verbindungsform hinzu.
1. Unterformen verbinden
### **Programmierbeispiel für Teilformen verbinden**
Verwenden Sie den folgenden Code in Ihrer Java-Anwendung, um die Unterformen von zwei verschiedenen Gruppenformen mit Aspose.Diagram for Java zu verbinden.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ConnectVisioSubShapes.class);   
// set sub shape ids
long shapeFromId = 2;
long shapeToId = 4;

// load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// access a particular page
Page page = diagram.getPages().getPage("Page-3");
       
// initialize connector shape
Shape shape = new Shape();
shape.getLine().getEndArrow().setValue(4);
shape.getLine().getLineWeight().setValue(0.01388);

// add shape
long connecter1Id = diagram.addShape(shape, "Dynamic connector", page.getID());
// connect sub-shapes
page.connectShapesViaConnector(shapeFromId, ConnectionPointPlace.RIGHT, shapeToId, ConnectionPointPlace.LEFT, connecter1Id);
// save Visio drawing
diagram.save(dataDir + "ConnectVisioSubShapes_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Holen Sie sich die Formen, die mit einer bestimmten Form verbunden sind**
[Visio Formen hinzufügen und verbinden](/diagram/de/java/add-and-connect-visio-shapes/) erklärt, wie man eine Form hinzufügt und sie mit anderen Formen in Microsoft Visio Diagrammen unter Verwendung von Aspose.Diagram for Java verbindet. Es ist auch möglich, Formen zu finden, die mit einer bestimmten Form verbunden sind.

 Die ConnectedShapes-Methode, die von der bereitgestellt wird[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) -Klasse kann verwendet werden, um die IDs der Shapes zu erhalten, die mit einem Shape verbunden sind. Die GetShape-Methode, verfügbar gemacht durch die[ShapeCollection](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shapecollection) Klasse, kann dann verwendet werden, um eine Form anhand ihrer ID zu finden.

Der folgende Code zeigt, wie man:

1. Laden Sie eine Beispieldatei.
1. Greifen Sie auf eine bestimmte Form zu.
1. Rufen Sie die Namen aller Formen ab, die mit der ausgewählten Form verbunden sind.
### **Holen Sie sich Shapes-Programmierbeispiel**
Verwenden Sie den folgenden Code in Ihrer Java-Anwendung, um alle Formen zu finden, die mit einer bestimmten Form verbunden sind, die Aspose.Diagram for Java verwendet.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetAllConnectedShapes.class);
// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get shape by id
Shape shape = diagram.getPages().getPage("Page-3").getShapes().getShape(16);
// get connected shapes
long[] connectedShapeIds = shape.connectedShapes(ConnectedShapesFlags.CONNECTED_SHAPES_ALL_NODES, null);

for (long id : connectedShapeIds)
{
    shape = diagram.getPages().getPage("Page-3").getShapes().getShape(id);
    System.out.println("ID: " + shape.getID() + "\t\t Name: " + shape.getName());
}

{{< /highlight >}}

