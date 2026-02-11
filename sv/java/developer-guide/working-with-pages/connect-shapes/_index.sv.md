---
title: Anslut former
type: docs
weight: 90
url: /sv/java/connect-shapes/
description: Det här avsnittet förklarar hur man kopplar två former med Aspose.Diagram for Java.
---
## **Anslut former**
Det här avsnittet förklarar hur man ansluter två former med Aspose.Diagram for Java.
### **Anslut former**
 De[connectShapesViaConnector](https://reference.aspose.com/diagram/java/com.aspose.diagram/page#connectShapesViaConnector(long,%20int,%20long,%20int,%20long) metod koppla två former via en kontakt i[Sida](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) klass.

Koden nedan visar hur man:

1. Skapa ett diagram från stencil.
1. Lägg till två rektanglar form på sidan.
1. Lägg till en kopplingsform på sidan.
1. Anslut de två rektanglarna med kontakten med hjälp av connectShapesViaConnector-metoden
1. spara diagram
#### **Connect Shapes programmeringsexempel**
Använd följande kod för att ansluta former med Aspose.Diagram for Java.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ConnectShapes.class);
String stencil = dataDir + "Basic Shapes.vss";

// create a diagram from stencil
Diagram diagram = new Diagram(stencil);
String connectorMaster = "Dynamic connector";
String rectangleMaster = "Rectangle";
// add two rectangles to page 0
long rectangle1 = diagram.addShape(2, 2, rectangleMaster, 0);
long rectangle2 = diagram.addShape(2, 4, rectangleMaster, 0);
// add a connector to page 0
Shape connector1 = new Shape();
long connecter1Id = diagram.addShape(connector1, connectorMaster, 0);
// connect the two rectangles with the connector
diagram.getPages().get(0).connectShapesViaConnector(rectangle1, ConnectionPointPlace.RIGHT, rectangle2, ConnectionPointPlace.BOTTOM, connecter1Id);

// If the connection of shapes has name, we also could use connection name to connect like below
//diagram.getPages().get(0).connectShapesViaConnector(shape1, "Port7", shape2, "Port21", connecter1Id);
// The code line above is equal to the below two lines
//diagram.getPages().get(0).glueShapeToConnectorBeginX(shape1, "Port7", connecter1Id);
//diagram.getPages().get(0).glueShapeToConnectorEndX(shape2, "Port21", connecter1Id);

// Save diagram
diagram.save(dataDir + "ConnectShapes_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```

|**Resultat**|
|:- |
|![ConnectShapes_out.vsdx](ConnectShapes.png)|
