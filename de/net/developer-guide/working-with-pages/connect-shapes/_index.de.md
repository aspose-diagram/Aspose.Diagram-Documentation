---
title: Formen verbinden
type: docs
weight: 90
url: /de/net/connect-shapes/
description: In diesem Abschnitt wird erklärt, wie Sie zwei Shapes mit Aspose.Diagram verbinden.
---
## **Formen verbinden**
In diesem Abschnitt wird erläutert, wie Sie zwei Formen mit Aspose.Diagram for .NET verbinden.
### **Formen verbinden**
 Das[ConnectShapesViaConnector](https://reference.aspose.com/diagram/net/aspose.diagram.page/connectshapesviaconnector/methods/1) method connect two shapes via a connector in the [Buchseite](http://www.aspose.com/api/net/diagram/aspose.diagram/page) Klasse.

Der folgende Code zeigt, wie man:

1. Erstellen Sie eine diagram aus der Schablone.
1. Fügen Sie der Seite zwei Rechtecke hinzu.
1. Fügen Sie der Seite ein Verbinder-Shape hinzu.
1. Verbinden Sie die beiden Rechtecke mit dem Connector mithilfe der ConnectShapesViaConnector-Methode
1. außer diagram
#### **Connect Shapes-Programmierbeispiel**
Verwenden Sie den folgenden Code in Ihrer .NET-Anwendung, um Formen mit Aspose.Diagram for .NET zu verbinden.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
string stencil = dataDir + "Basic Shapes.vss";

// create a diagram from stencil
Diagram diagram = new Diagram(stencil);
string connectorMaster = "Dynamic connector";
string rectangleMaster = "Rectangle";
// add two rectangles to page 0
long rectangle1 = diagram.AddShape(2, 2, rectangleMaster, 0);
long rectangle2 = diagram.AddShape(2, 4, rectangleMaster, 0);
// add a connector to page 0
Shape connector1 = new Shape();
long connecter1Id = diagram.AddShape(connector1, connectorMaster, 0);
// connect the two rectangles with the connector
diagram.Pages[0].ConnectShapesViaConnector(rectangle1, ConnectionPointPlace.Right, rectangle2, ConnectionPointPlace.Bottom, connecter1Id);

// If the connection of shapes has name, we also could use connection name to connect like below
//diagram.Pages[0].ConnectShapesViaConnector(shape1, "Port7", shape2, "Port21", connecter1Id);
// The code line above is equal to the below two lines
//diagram.Pages[0].GlueShapeToConnectorBeginX(shape1, "Port7", connecter1Id);
//diagram.Pages[0].GlueShapeToConnectorEndX(shape2, "Port21", connecter1Id);

// Save diagram
diagram.Save(dataDir + "ConnectShapes_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```

|**Ergebnis**|
|:- |
|![ConnectShapes_out.vsdx](ConnectShapes.png)|
