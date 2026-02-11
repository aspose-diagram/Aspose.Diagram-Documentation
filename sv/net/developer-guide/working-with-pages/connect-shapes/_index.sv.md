---
title: Anslut former
type: docs
weight: 90
url: /sv/net/connect-shapes/
description: Det här avsnittet förklarar hur man kopplar två former med Aspose.Diagram.
---
## **Anslut former**
Det här avsnittet förklarar hur man ansluter två former med Aspose.Diagram for .NET.
### **Anslut former**
 De[ConnectShapesViaConnector](https://reference.aspose.com/diagram/net/aspose.diagram.page/connectshapesviaconnector/methods/1) metod koppla två former via en kontakt i[Sida](http://www.aspose.com/api/net/diagram/aspose.diagram/page) klass.

Koden nedan visar hur man:

1. Skapa ett diagram från stencil.
1. Lägg till två rektanglar form på sidan.
1. Lägg till en kopplingsform på sidan.
1. Anslut de två rektanglarna med kontakten med hjälp av ConnectShapesViaConnector-metoden
1. spara diagram
#### **Connect Shapes programmeringsexempel**
Använd följande kod i din .NET-applikation för att ansluta former med Aspose.Diagram for .NET.

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

|**Resultat**|
|:- |
|![ConnectShapes_out.vsdx](ConnectShapes.png)|
