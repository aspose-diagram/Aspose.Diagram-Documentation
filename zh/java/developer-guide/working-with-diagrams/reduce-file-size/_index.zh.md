---
title: 减小文件大小
type: docs
weight: 50
url: /zh/java/reduce-file-size/
description: 本节介绍如何使用 Aspose.Diagram 减小 diagram 的文件大小。
---
## **减小文件大小**
 Aspose.Diagram for Java API 允许开发人员从 diagram 中删除隐藏信息以减小文件大小。
这[页](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page)对象表示前景页面或背景页面的绘图区域。为了减小文件大小，您可以使用[删除隐藏信息项](https://reference.aspose.com/diagram/java/com.aspose.diagram/RemoveHiddenInfoItem)中的属性**移除隐藏信息()**的方法[Diagram](https://reference.aspose.com/diagram/java)班级。下面的代码示例显示了如何从 diagram 中删除隐藏信息。

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ReduceFileSize.class);

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Remove hidden information from diagram
diagram.removeHiddenInformation((int)(RemoveHiddenInfoItem.SHAPES | RemoveHiddenInfoItem.MASTERS));
{{< /highlight >}}
```
