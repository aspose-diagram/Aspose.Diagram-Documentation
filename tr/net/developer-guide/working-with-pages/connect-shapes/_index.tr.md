---
title: Şekilleri Bağlayın
type: docs
weight: 90
url: /tr/net/connect-shapes/
description: Bu bölümde, iki şeklin Aspose.Diagram ile nasıl bağlanacağı açıklanmaktadır.
---
## **Şekilleri Bağlayın**
Bu bölümde, Aspose.Diagram for .NET kullanılarak iki şeklin nasıl birleştirileceği açıklanmaktadır.
### **Şekilleri Bağlayın**
 bu[ConnectShapesViaConnector](https://reference.aspose.com/diagram/net/aspose.diagram.page/connectshapesviaconnector/methods/1) yöntem iki şekli birleştirir via bir konektör[Sayfa](http://www.aspose.com/api/net/diagram/aspose.diagram/page) sınıf.

Aşağıdaki kod nasıl yapılacağını gösterir:

1. Şablondan bir diagram oluşturun.
1. Sayfaya iki dikdörtgen şekli ekleyin.
1. Sayfaya bağlayıcı şekli ekleyin.
1. ConnectShapesViaConnector yöntemini kullanarak iki dikdörtgeni bağlayıcıyla birleştirin
1. kaydet diagram
#### **Connect Shapes Programlama Örneği**
Aspose.Diagram for .NET kullanarak şekilleri bağlamak için .NET uygulamanızda aşağıdaki kodu kullanın.

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

|**Sonuç**|
|:- |
|![ConnectShapes_out.vsdx](ConnectShapes.png)|
