---
title: Connecter les formes
type: docs
weight: 90
url: /fr/net/connect-shapes/
description: Cette section explique comment connecter deux formes avec Aspose.Diagram.
---
## **Connecter les formes**
Cette section explique comment connecter deux formes en utilisant Aspose.Diagram for .NET.
### **Connecter les formes**
 La[ConnectShapesViaConnectorConnectShapesViaConnector](https://reference.aspose.com/diagram/net/aspose.diagram.page/connectshapesviaconnector/methods/1) method connect two shapes via a connector in the [Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page) classer.

Le code ci-dessous montre comment :

1. Créez un diagram à partir du gabarit.
1. Ajoutez la forme de deux rectangles à la page.
1. Ajoutez une forme de connecteur à la page.
1. Connectez les deux rectangles avec le connecteur à l'aide de la méthode ConnectShapesViaConnector
1. enregistrer diagram
#### **Exemple de programmation Connect Shapes**
Utilisez le code suivant dans votre application .NET pour connecter des formes à l'aide de Aspose.Diagram for .NET.


{{< highlight csharp >}}
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


|**Résultat**|
|:- |
|![ConnectShapes_out.vsdx](ConnectShapes.png)|
