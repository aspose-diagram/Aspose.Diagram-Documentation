---
title: 检索字体信息
type: docs
weight: 80
url: /zh/net/retrieving-font-information/
---
## **VSTO**
下面是检索字体信息的代码：

{{< highlight "cs" >}}

  foreach (Font font in Application.ActiveDocument.Fonts)

 {

    //Display information about the fonts

    MessageBox.Show(font.Name);

 }

{{< /highlight >}}
## **Aspose.Diagram**
{{% alert color="primary" %}} 

Aspose.Diagram 具有从中检索有关构成 diagram 的元素的信息的机制[页数](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection) , 模板,[连接器](/diagram/zh/net/retrieving-connector-information/)还有字体。本文介绍如何找出 diagram 中使用了哪些字体。

{{% /alert %}} 

这[字体](https://reference.aspose.com/diagram/net/aspose.diagram/font)对象表示应用于文档中的文本或可在系统上使用的字体。

字体对象将名称（例如“Arial”）映射到字体 ID（例如 3），字体 ID Microsoft Visio 存储在形状的字符部分的字体单元格中，该形状包含使用该字体设置格式的文本。当在不同系统上打开文档或安装或删除字体时，字体 ID 可能会发生变化。

{{< highlight "cs" >}}

  //Call the diagram constructor to load diagram from a VDX file

 Diagram vdxDiagram = new Diagram(@"E:\Aspose\Aspose Vs VSTO\Aspose.Diagram Vs VSTO Visio v1.1\Sample Files\Drawing1.vdx");

 foreach (Aspose.Diagram.Font font in vdxDiagram.Fonts)

 {

    //Display information about the fonts

    Console.WriteLine(font.Name);

 }

{{< /highlight >}}
## **下载示例代码**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **下载运行代码**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Retrieving%20Font%20Information)
