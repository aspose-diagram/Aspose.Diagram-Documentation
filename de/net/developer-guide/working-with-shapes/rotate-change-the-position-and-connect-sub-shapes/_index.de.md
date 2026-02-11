---
title: Drehen, ändern Sie die Position und verbinden Sie Unterformen
type: docs
weight: 30
url: /de/net/rotate-change-the-position-and-connect-sub-shapes/
description: In diesem Abschnitt wird erläutert, wie Sie eine visio-Form mit Aspose.Diagram drehen.
---
## **Drehen Sie eine Form mit einem geeigneten Winkel**
 Mit Aspose.Diagram for .NET können Sie eine Form in einen beliebigen Winkel drehen. Die SetAngle-Methode, die von der bereitgestellt wird[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) -Klasse kann verwendet werden, um eine Form in jeden gewünschten Winkel zu drehen. Es nimmt einen einzelnen Parameter als Winkel an.
### **Drehen eines Formprogrammierungsbeispiels**
Verwenden Sie den folgenden Code in Ihrer .NET-Anwendung, um eine Form mit Aspose.Diagram for .NET zu drehen.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");
// Get shape by id
Shape shape = page.Shapes.GetShape(16);

// Add a shape and set the angle
shape.SetAngle(190);

// Save diagram
diagram.Save(dataDir + "RotateVisioShape_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Ändern Sie die Position einer Form**
 Das[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Mit der Klasse können Sie die Position einer Form ändern. Die Verbindungslinie passt sich automatisch an, wenn die Form an eine andere Position verschoben wird. Die Move- und MoveTo-Methoden, die von verfügbar gemacht werden[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Klasse, unterstützen Sie das Ändern der Position einer Form als Teil einer Gruppe oder nicht. Die Codebeispiele in diesem Artikel verschieben eine Form auf der Seite.

Der Vorgang zum Verschieben einer Form ist:

1. Laden Sie eine diagram.
1. Finden Sie eine bestimmte Form.
1. Verschieben Sie die Form an einen anderen Ort
1. Speichern Sie die diagram.
### **Beispiel für die Programmierung der Position ändern**
Das folgende Code-Snippet zeigt, wie die Form verschoben wird. Der Code ruft eine Visio-Seite nach Name und Form nach ID 16 ab und verschiebt ihre Position.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");
// Get shape by id
Shape shape = page.Shapes.GetShape(16);
// Move shape from its position, it adds values in coordinates
shape.Move(1, 1);

// Save diagram
diagram.Save(dataDir + "MoveVisioShape_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Verbinden Sie Unterformen der Gruppen**
 In diesem Thema wird erläutert, wie zwei Unterformen von zwei verschiedenen Gruppenformen in Microsoft Visio-Diagrammen mithilfe von Aspose.Diagram for .NET verbunden werden. Die ConnectShapesViaConnector-Methode, die von der[Buchseite](http://www.aspose.com/api/net/diagram/aspose.diagram/page) Klasse kann verwendet werden, um die Shapes über ihre IDs zu verbinden. Die AddShape-Methode, verfügbar gemacht durch die[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)Klasse, kann verwendet werden, um eine Form hinzuzufügen.

Der folgende Code zeigt, wie man:

1. Laden Sie eine Beispieldatei.
1. Greifen Sie auf eine bestimmte Seite zu.
1. Fügen Sie der ausgewählten Seite eine dynamische Verbindungsform hinzu.
1. Unterformen verbinden
### **Programmierbeispiel für Teilformen verbinden**
Verwenden Sie den folgenden Code in Ihrer .NET-Anwendung, um die Unterformen von zwei verschiedenen Gruppenformen mit Aspose.Diagram for .NET zu verbinden.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Set sub shape ids
long shapeFromId = 2;
long shapeToId = 4;

// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Access a particular page
Page page = diagram.Pages.GetPage("Page-3");
           
// Initialize connector shape
Shape shape = new Shape();
shape.Line.EndArrow.Value = 4;
shape.Line.LineWeight.Value = 0.01388;

// Add shape
long connecter1Id = diagram.AddShape(shape, "Dynamic connector", page.ID);
// Connect sub-shapes
page.ConnectShapesViaConnector(shapeFromId, ConnectionPointPlace.Right, shapeToId, ConnectionPointPlace.Left, connecter1Id);
// Save Visio drawing
diagram.Save(dataDir + "ConnectVisioSubShapes_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Holen Sie sich die Formen, die mit einer bestimmten Form verbunden sind**
[Visio Formen hinzufügen und verbinden](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/) erklärt, wie man eine Form hinzufügt und sie mit anderen Formen in Microsoft Visio Diagrammen unter Verwendung von Aspose.Diagram for .NET verbindet. Es ist auch möglich, Formen zu finden, die mit einer bestimmten Form verbunden sind.

 Die ConnectedShapes-Methode, die von der bereitgestellt wird[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) -Klasse kann verwendet werden, um die IDs der Shapes zu erhalten, die mit einem Shape verbunden sind. Die GetShape-Methode, verfügbar gemacht durch die[ShapeCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/shapecollection) Klasse, kann dann verwendet werden, um eine Form anhand ihrer ID zu finden.

Der folgende Code zeigt, wie man:

1. Laden Sie eine Beispieldatei.
1. Greifen Sie auf eine bestimmte Form zu.
1. Rufen Sie die Namen aller Formen ab, die mit der ausgewählten Form verbunden sind.
### **Holen Sie sich Shapes-Programmierbeispiel**
Verwenden Sie den folgenden Code in Ihrer .NET-Anwendung, um alle Formen zu finden, die mit einer bestimmten Form verbunden sind, die Aspose.Diagram for .NET verwendet.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get shape by id
Shape shape = diagram.Pages.GetPage("Page-3").Shapes.GetShape(16);
// Get connected shapes
long[] connectedShapeIds = shape.ConnectedShapes(ConnectedShapesFlags.ConnectedShapesAllNodes, null);

foreach (long id in connectedShapeIds)
{
    shape = diagram.Pages.GetPage("Page-3").Shapes.GetShape(id);
    Console.WriteLine("ID: " + shape.ID + "\t\t Name: " + shape.Name);
}

{{< /highlight >}}
```
