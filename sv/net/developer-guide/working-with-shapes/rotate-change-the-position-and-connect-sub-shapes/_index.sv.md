---
title: Rotera, ändra position och anslut delformer
type: docs
weight: 30
url: /sv/net/rotate-change-the-position-and-connect-sub-shapes/
description: Det här avsnittet förklarar hur man roterar en visio-form med Aspose.Diagram.
---
## **Rotera en form med lämplig vinkel**
 Aspose.Diagram for .NET låter dig rotera en form till vilken vinkel som helst. SetAngle-metoden exponerad av[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) klass kan användas för att rotera en form till valfri vinkel. Det tar en enda parameter som en vinkel.
### **Rotera ett formprogrammeringsprov**
Använd följande kod i din .NET-applikation för att rotera en form med Aspose.Diagram for .NET.

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
## **Ändra positionen för en form**
 De[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Klass låter dig ändra positionen för en form. Anslutningslinjen justeras automatiskt när formen flyttas till en annan position. Metoderna Move och MoveTo, exponerade av[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) klass, stöd för att ändra positionen för en form som en del av en grupp eller inte. Kodexemplen i den här artikeln flyttar en form på sidan.

Processen för att flytta en form är:

1. Ladda ett diagram.
1. Hitta en viss form.
1. Flytta formen till en annan plats
1. Spara diagram.
### **Ändra positionsprogrammeringsexempel**
Kodavsnittet nedan visar hur du flyttar formen. Koden hämtar en Visio-sida med namn och form med ID 16 och flyttar dess position.

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
## **Anslut underformer av grupperna**
 Det här ämnet utvecklar hur man kopplar samman två underformer av två olika gruppformer i Microsoft Visio diagram med Aspose.Diagram for .NET. ConnectShapesViaConnector-metoden exponerad av[Sida](http://www.aspose.com/api/net/diagram/aspose.diagram/page) klass kan användas för att koppla ihop formerna med deras ID. AddShape-metoden, exponerad av[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)klass, kan användas för att lägga till en form.

Koden nedan visar hur man:

1. Ladda en exempelfil.
1. Gå till en viss sida.
1. Lägg till en dynamisk kopplingsform på den valda sidan.
1. Anslut underformer
### **Connect Sub-shapes programmeringsexempel**
Använd följande kod i din .NET-applikation för att ansluta underformerna till två olika gruppformer med Aspose.Diagram for .NET.

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
## **Få formerna kopplade till en viss form**
[Lägg till och anslut Visio Former](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/) förklarar hur man lägger till en form och kopplar den till andra former i Microsoft Visio diagram med Aspose.Diagram for .NET. Det är också möjligt att hitta former som är kopplade till en specifik form.

 ConnectedShapes-metoden exponerad av[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) klass kan användas för att få ID:n för formerna kopplade till en form. GetShape-metoden, exponerad av[ShapeCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/shapecollection) klass, kan sedan användas för att hitta en form med dess ID.

Koden nedan visar hur man:

1. Ladda en exempelfil.
1. Få tillgång till en viss form.
1. Hämta namnen på alla former som är kopplade till den valda formen.
### **Få formprogrammeringsexempel**
Använd följande kod i din .NET-applikation för att hitta alla former som är kopplade till en specifik form med Aspose.Diagram for .NET.

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
