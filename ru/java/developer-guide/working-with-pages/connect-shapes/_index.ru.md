---
title: Соедините фигуры
type: docs
weight: 90
url: /ru/java/connect-shapes/
description: В этом разделе объясняется, как соединить две фигуры с помощью Aspose.Diagram for Java.
---
## **Соедините фигуры**
В этом разделе объясняется, как соединить две фигуры с помощью Aspose.Diagram for Java.
### **Соедините фигуры**
[connectShapesViaConnector](https://reference.aspose.com/diagram/java/com.aspose.diagram/page#connectShapesViaConnector(long,%20int,%20long,%20int,%20long) ) способ соединения двух форм via разъема в[Страница](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) учебный класс.

В приведенном ниже коде показано, как:

1. Создайте diagram из трафарета.
1. Добавьте на страницу два прямоугольника.
1. Добавьте фигуру соединителя на страницу.
1. Соедините два прямоугольника соединителем, используя метод connectShapesViaConnector.
1. сохранить diagram
#### **Образец программирования Connect Shapes**
Используйте следующий код для соединения фигур с помощью Aspose.Diagram for Java.

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

|**Результат**|
|:- |
|![ConnectShapes_out.vsdx](ConnectShapes.png)|
