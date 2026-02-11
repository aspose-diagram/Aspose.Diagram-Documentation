---
title: Conectar formas
type: docs
weight: 90
url: /es/java/connect-shapes/
description: Esta sección explica cómo conectar dos formas con Aspose.Diagram for Java.
---
## **Conectar formas**
Esta sección explica cómo conectar dos formas usando Aspose.Diagram for Java.
### **Conectar formas**
 los[connectShapesViaConector](https://reference.aspose.com/diagram/java/com.aspose.diagram/page#connectShapesViaConnector(long,%20int,%20long,%20int,%20long)) method connect two shapes via a connector in the [Página](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) clase.

El siguiente código muestra cómo:

1. Cree un diagram a partir de la plantilla.
1. Agregue dos formas de rectángulos a la página.
1. Agregue una forma de conector a la página.
1. Conecte los dos rectángulos con el conector usando el método connectShapesViaConnector
1. guardar diagram
#### **Ejemplo de programación de Connect Shapes**
Use el siguiente código para conectar formas usando Aspose.Diagram for Java.

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

|**Resultado**|
|:- |
|![ConnectShapes_out.vsdx](ConnectShapes.png)|
