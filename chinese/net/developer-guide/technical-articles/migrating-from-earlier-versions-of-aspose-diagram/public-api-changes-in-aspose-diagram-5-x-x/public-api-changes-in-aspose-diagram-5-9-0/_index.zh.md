---
title: 公共 API Aspose.Diagram 5.9.0 的变化
type: docs
weight: 10
url: /zh/net/public-api-changes-in-aspose-diagram-5-9-0/
---
{{% alert color="primary" %}} 

本文档描述了 Aspose.Diagram API 从版本 5.8.0 到 5.9.0 的变化，模块/应用程序开发人员可能会感兴趣。它不仅包括新的和更新的公共方法，还包括对 Aspose.Diagram 中幕后行为的任何更改的描述。

{{% /alert %}} 
## **Save Resultant HTML to a Stream**
新的 Save 方法已添加到 Diagram 类中。它有两个参数，流对象和保存文件格式。
示例代码：

**C#**

{{< highlight "java" >}}

 // load an existing visio diagram

Diagram diagram = new Diagram("Basic Flowchart.vsd");

// save resultant HTML directly to a stream

MemoryStream stream = new MemoryStream();

diagram.Save(stream, SaveFileFormat.HTML);

{{< /highlight >}}

**虚拟机**

{{< highlight "java" >}}

 ' load an existing visio diagram

Dim diagram As Diagram = New Diagram("Basic Flowchart.vsd")

' save resultant HTML directly to a stream

MemoryStream stream = new MemoryStream()

diagram.Save(stream, SaveFileFormat.HTML)

{{< /highlight >}}
## **从另一个 Visio 复制主题和 PageSheet**
Diagram类提供了CopyTheme方法，PageSheet类提供了Copy方法来完成复制形状等操作任务。
示例代码：[从现有的 Visio 复制形状](/diagram/zh/net/add-retrieve-copy-and-read-visio-shape-data/)
## **在 SaveFileFormat 中添加了 VSTX 和 VSSX 保存选项**
之前Aspose.Diagram API已经支持读写VSDX格式，现在我们也增加了对VSTX和VSSX格式写图的支持。示例代码：

**C#**

{{< highlight "java" >}}

 // save diagram in the VSTX format

diagram.Save("C:\\temp\\Output.vstx", SaveFileFormat.VSTX);

// save diagram in the VSSX format

diagram.Save("C:\\temp\\Output.vssx", SaveFileFormat.VSSX);

{{< /highlight >}}

**虚拟机**

{{< highlight "java" >}}

 ' save diagram in the VSTX format

diagram.Save("C:\\temp\\Output.vstx", SaveFileFormat.VSTX)

' save diagram in the VSSX format

diagram.Save("C:\\temp\\Output.vssx", SaveFileFormat.VSSX)

{{< /highlight >}}
## **VSSX 在 LoadFileFormat 中添加了阅读选项**
之前Aspose.Diagram API支持读写VSDX格式，现在我们也增加了读取VSSX模板格式的支持。示例代码：

**C#**

{{< highlight "java" >}}

 // read VSSX stencil

Diagram diagram = new Diagram(@"C:\temp\Stencil.vssx", LoadFileFormat.VSSX);

{{< /highlight >}}

**虚拟机**

{{< highlight "java" >}}

 ' read VSSX stencil

Diagram diagram = new Diagram(@"C:\temp\Stencil.vssx", LoadFileFormat.VSSX)

{{< /highlight >}}
