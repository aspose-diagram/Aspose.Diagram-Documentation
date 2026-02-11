---
title: 将 Visio 形状转换为图像
type: docs
weight: 10
url: /zh/java/convert-a-visio-shape-to-image/
description: 本节介绍如何将 visio 形状转换为具有 Aspose.Diagram 的图像。
---
## **将 visio 形状转换为图像**
公开的 ToImage 方法[形状](http://www.aspose.com/api/java/diagram/com.aspose.diagram/shape)类可用于转换为图像。

下面的代码显示了如何：

1. 加载示例 diagram。
1. 获取特定页面。
1. 得到一个特定的形状。
1. 将形状转换为图像。
### **形状到图像**
在您的 Java 应用程序中使用以下代码将 visio 形状转换为图像。

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ShapeToImage.class); 
// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToImage.vsdx");

// Get a particular page
Page page = diagram.getPages().get(0);

// Get a particular shape
Shape shape = page.getShapes().get(0);

// Shape to image
com.aspose.diagram.ImageSaveOptions option = new com.aspose.diagram.ImageSaveOptions(SaveFileFormat.PNG);
shape.toImage("out.png",option);
{{< /highlight >}}
```


