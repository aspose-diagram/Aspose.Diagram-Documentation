---
title: Connecter les formes
type: docs
weight: 90
url: /fr/java/connect-shapes/
description: Cette section explique comment connecter deux formes avec Aspose.Diagram for Java.
---
## **Connecter les formes**
Cette section explique comment connecter deux formes en utilisant Aspose.Diagram for Java.
### **Connecter les formes**
 La[connectShapesViaConnectorconnectShapesViaConnector](https://reference.aspose.com/diagram/java/com.aspose.diagram/page#connectShapesViaConnector(long,%20int,%20long,%20int,%20long)) method connect two shapes via a connector in the [Page](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) classer.

Le code ci-dessous montre comment :

1. Créez un diagram à partir du gabarit.
1. Ajoutez la forme de deux rectangles à la page.
1. Ajoutez une forme de connecteur à la page.
1. Connectez les deux rectangles avec le connecteur à l'aide de la méthode connectShapesViaConnector
1. enregistrer diagram
#### **Exemple de programmation Connect Shapes**
Utilisez le code suivant pour connecter des formes à l'aide de Aspose.Diagram for Java.


{{< highlight java >}}
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


|**Résultat**|
|:- |
|![ConnectShapes_out.vsdx](ConnectShapes.png)|
