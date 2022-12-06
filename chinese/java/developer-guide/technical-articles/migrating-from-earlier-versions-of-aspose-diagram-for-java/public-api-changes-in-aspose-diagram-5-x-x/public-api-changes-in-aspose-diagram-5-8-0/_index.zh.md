---
title: 公共 API Aspose.Diagram 5.8.0 的变化
type: docs
weight: 20
url: /zh/java/public-api-changes-in-aspose-diagram-5-8-0/
---
{{% alert color="primary" %}} 

本文档描述了 Aspose.Diagram API 从版本 5.7.0 到 5.8.0 的变化，模块/应用程序开发人员可能会感兴趣。它不仅包括新的和更新的公共方法，还包括对 Aspose.Diagram 中幕后行为的任何更改的描述。

{{% /alert %}} 
### **在 HTMLSaveOptions 中添加 SaveToolBar 选项**
新的 SaveToolBar 选项已添加到 HTMLSaveOptions 类中。它指定是否保存工具栏。默认值是true。示例代码：

**Java**

{{< highlight "java" >}}

 // initialize HTMLSaveOptions class object

HTMLSaveOptions opts = new HTMLSaveOptions();

// set save toolbar option

opts.setSaveToolBar(false);

{{< /highlight >}}
### **VSDX 在 SaveFileFormat 中添加了保存选项**
之前Aspose.Diagram API支持读取VSDX格式，现在我们增加了VSDX格式写图的支持。示例代码：

**Java**

{{< highlight "java" >}}

 // save diagram in the VSDX format

diagram.save("C:\\temp\\Output.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **ShapeCollection 类中添加了组方法**
开发人员现在可以使用 Aspose.Diagram API 在 Visio diagram 中将多个形状组合在一起。示例代码：

**Java**

{{< highlight "java" >}}

 // load a Visio diagram

Diagram diagram = new Diagram("c:\\temp\\test.vsd");

// Initialize an array of shapes

Shape[]shapes = new Shape[2];

// extract and assign shapes to the array

shapes[0]= diagram.getPages().get(0).getShapes().getShape(1);

shapes[1]= diagram.getPages().get(0).getShapes().getShape(2);

// mark array shapes as group

diagram.getPages().get(0).getShapes().group(shapes);

// save visio diagram

diagram.save("c:\\temp\\out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
