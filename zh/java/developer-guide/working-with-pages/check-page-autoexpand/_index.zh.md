---
title: 检查页面自动扩展
type: docs
weight: 10
url: /zh/java/check-page-autoexpand/
description: 本节介绍如何检查或更改页面是否在带有 Aspose.Diagram 的 visio 文件中自动展开。
---
## **检查页面自动扩展**

这[页](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)对象表示前景页面或背景页面的绘图区域。公开的 Pages 属性[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram)类支持 Aspose.Diagram.Page 对象的集合。
这[页面道具](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageProps)对象表示页面属性，例如页面宽度、高度和比例。此属性可用于检查页面的自动扩展。

使用 PageProps 属性检查页面的自动展开。
### **检查页面自动扩展编程示例**
以下代码检查页面从 diagram 自动扩展。


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CheckChangeAutoExpand.class);
      
// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Page page = diagram.getPages().getPage("Page-2");
// Get Page autoexpand
boolean isAutoExpand = page.getPageSheet().getPageProps().getDrawingResizeType().getValue() == DrawingResizeTypeValue.AUTOMATICALLY ? true : false;
//Set Page autoexpand
page.getPageSheet().getPageProps().getDrawingResizeType().setValue(DrawingResizeTypeValue.NOT_AUTOMATICALLY);

// Save Visio
diagram.save(dataDir + "SetAutoExpand_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

