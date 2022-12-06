---
title: 公共 API Aspose.Diagram 5.9.0 的变化
type: docs
weight: 10
url: /zh/java/public-api-changes-in-aspose-diagram-5-9-0/
---
{{% alert color="primary" %}} 

本文档描述了 Aspose.Diagram API 从版本 5.8.0 到 5.9.0 的变化，模块/应用程序开发人员可能会感兴趣。它不仅包括新的和更新的公共方法，还包括对 Aspose.Diagram 中幕后行为的任何更改的描述。

{{% /alert %}} 
### **将生成的 HTML 保存到流中**
新的保存方法已添加到 Diagram 类中。它有两个参数，流对象和保存文件格式。
示例代码：

**Java**

{{< highlight "java" >}}

 // Call the diagram constructor to load diagram from a VSD file

Diagram diagram = new Diagram("Basic Flowchart.vsd");

// save resultant HTML directly to a stream

ByteArrayOutputStream dstStream = new ByteArrayOutputStream();

diagram.save(dstStream, SaveFileFormat.HTML);

// In you want to read the result into a Diagram object again, in Java you need to get the

// data bytes and wrap into an input stream.

ByteArrayInputStream srcStream = new ByteArrayInputStream(dstStream.toByteArray());

{{< /highlight >}}
### **从另一个 Visio 复制主题和 PageSheet**
Diagram类提供了CopyTheme方法，PageSheet类提供了Copy方法来完成复制形状等操作任务。
示例代码：[从现有的 Visio 复制形状](/diagram/zh/java/working-with-visio-shape-data/#copy-shapes-from-an-existing-visio)
### **在 SaveFileFormat 中添加了 VSTX 和 VSSX 保存选项**
之前Aspose.Diagram API已经支持读写VSDX格式，现在我们也增加了对VSTX和VSSX格式写图的支持。示例代码：

**Java**

{{< highlight "java" >}}

 // save diagram in the VSTX format

diagram.save("C:\\temp\\Output.vstx", SaveFileFormat.VSTX);

// save diagram in the VSSX format

diagram.save("C:\\temp\\Output.vssx", SaveFileFormat.VSSX);

{{< /highlight >}}
### **VSSX 在 LoadFileFormat 中添加了阅读选项**
之前Aspose.Diagram API支持读写VSDX格式，现在我们也增加了读取VSSX模板格式的支持。示例代码：

**Java**

{{< highlight "java" >}}

 // read VSSX stencil

Diagram diagram = new Diagram("C:\\temp\\Stencil.vssx", LoadFileFormat.VSSX);

{{< /highlight >}}
