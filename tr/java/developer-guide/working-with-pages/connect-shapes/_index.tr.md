---
title: Şekilleri Bağlayın
type: docs
weight: 90
url: /tr/java/connect-shapes/
description: Bu bölümde, Aspose.Diagram for Java ile iki şeklin nasıl birleştirileceği açıklanmaktadır.
---
## **Şekilleri Bağlayın**
Bu bölümde, Aspose.Diagram for Java kullanılarak iki şeklin nasıl birleştirileceği açıklanmaktadır.
### **Şekilleri Bağlayın**
 bu[bağlantıShapesViaConnector](https://reference.aspose.com/diagram/java/com.aspose.diagram/page#connectShapesViaConnector(long,%20int,%20long,%20int,%20long) ) yöntem iki şekli birleştirir via bir konektör[Sayfa](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) sınıf.

Aşağıdaki kod nasıl yapılacağını gösterir:

1. Şablondan bir diagram oluşturun.
1. Sayfaya iki dikdörtgen şekli ekleyin.
1. Sayfaya bağlayıcı şekli ekleyin.
1. connectShapesViaConnector yöntemini kullanarak iki dikdörtgeni bağlayıcıyla birleştirin
1. kaydet diagram
#### **Connect Shapes Programlama Örneği**
Aspose.Diagram for Java kullanarak şekilleri bağlamak için aşağıdaki kodu kullanın.

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

|**Sonuç**|
|:- |
|![ConnectShapes_out.vsdx](ConnectShapes.png)|
