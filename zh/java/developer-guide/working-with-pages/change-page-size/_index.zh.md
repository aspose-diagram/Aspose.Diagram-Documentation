---
title: 更改页面大小
type: docs
weight: 10
url: /zh/java/change-page-size/
description: 本节介绍如何使用 Aspose.Diagram 更改 visio 文件中的页面大小。
---
## **更改页面大小**

这[页](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)对象表示前景页面或背景页面的绘图区域。公开的 Pages 属性[Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/diagram)类支持 Aspose.Diagram.Page 对象的集合。
这[页面道具](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageProps)对象表示页面属性，例如页面宽度、高度和比例。此属性可用于更改页面大小。

使用 PageProps 属性更改页面大小。
### **设置页面大小编程示例**
以下代码段从 diagram 更改页面大小。


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ChangeVisioPageSize.class);
      
// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Page page = diagram.getPages().getPage("Flow 1");
// Set Page Size
page.getPageSheet().getPageProps().getPageHeight().setValue(8);
page.getPageSheet().getPageProps().getPageWidth().setValue(11);

// Save Visio
diagram.save(dataDir + "SetPageSize_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

