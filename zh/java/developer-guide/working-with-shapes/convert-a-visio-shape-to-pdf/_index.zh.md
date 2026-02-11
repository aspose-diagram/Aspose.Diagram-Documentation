---
title: 将 Visio 形状转换为 Pdf
type: docs
weight: 10
url: /zh/java/convert-a-visio-shape-to-pdf/
description: 本节介绍如何使用 Aspose.Diagram 将 visio 形状转换为 pdf。
---
## **将 visio 形状转换为 pdf**
公开的 ToPdf 方法[形状](http://www.aspose.com/api/java/diagram/com.aspose.diagram/shape)类可用于转换为pdf。

下面的代码显示了如何：

1. 加载示例 diagram。
1. 获取特定页面。
1. 得到一个特定的形状。
1. 将形状转换为 pdf。
### **形状转 Pdf**
在您的 Java 应用程序中使用以下代码将 visio 形状转换为 pdf。


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ShapeToPdf.class); 
// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToPdf.vsdx");

// Get a particular page
Page page = diagram.getPages().get(0);

// Get a particular shape
Shape shape = page.getShapes().get(0);

// Shape to Pdf
shape.toPdf("out.pdf");
{{< /highlight >}}



