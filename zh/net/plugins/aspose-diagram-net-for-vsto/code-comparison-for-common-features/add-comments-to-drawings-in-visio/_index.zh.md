---
title: 在 Visio 中为图纸添加注释
type: docs
weight: 40
url: /zh/net/add-comments-to-drawings-in-visio/
---
## **VSTO**
下面是diagram中添加注释的代码：

{{< highlight "cs" >}}

  Page mypage= Application.ActiveDocument.Pages[1];

 mypage.Comments.Add("Test");

{{< /highlight >}}
## **Aspose.Diagram**
{{% alert color="primary" %}} 

Aspose.Diagram for .NET 允许您在 diagram 页面的任何位置放置评论。

{{% /alert %}} 

Page 类公开的 AddComment 方法允许您向绘图页添加注释。它采用 X 和 Y 坐标以及注释字符串。下面是代码片段：

{{< highlight "cs" >}}

  // Load diagram

 Diagram diagram = new Diagram("Drawing1.vsd");

 // Add comment

 diagram.Pages[0].AddComment(7.205905511811023, 3.880708661417323, "test@");

 // Save diagram

 diagram.Save("Output.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
## **下载示例代码**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **下载运行代码**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Add%20Comment)
