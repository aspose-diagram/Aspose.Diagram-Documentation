---
title: Conectar formas
type: docs
weight: 90
url: /es/net/connect-shapes/
description: Esta sección explica cómo conectar dos formas con Aspose.Diagram.
---
## **Conectar formas**
Esta sección explica cómo conectar dos formas usando Aspose.Diagram for .NET.
### **Conectar formas**
 los[ConnectShapesViaConector](https://reference.aspose.com/diagram/net/aspose.diagram.page/connectshapesviaconnector/methods/1) method connect two shapes via a connector in the [Página](http://www.aspose.com/api/net/diagram/aspose.diagram/page) clase.

El siguiente código muestra cómo:

1. Cree un diagram a partir de la plantilla.
1. Agregue dos formas de rectángulos a la página.
1. Agregue una forma de conector a la página.
1. Conecte los dos rectángulos con el conector usando el método ConnectShapesViaConnector
1. guardar diagram
#### **Ejemplo de programación de Connect Shapes**
Use el siguiente código en su aplicación .NET para conectar formas usando Aspose.Diagram for .NET.

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

|**Resultado**|
|:- |
|![ConnectShapes_out.vsdx](ConnectShapes.png)|
