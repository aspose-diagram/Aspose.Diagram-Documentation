---
title: 撰写文件摘要
type: docs
weight: 70
url: /zh/net/writing-document-summary/
---
## **VSTO**
下面是写Visio文档摘要的代码：

{{< highlight "cs" >}}

  Application.ActiveDocument.Creator = "Zeeshan";

 Application.ActiveDocument.Company = "Aspose";

 Application.ActiveDocument.Category = "Drawing 2D";

 Application.ActiveDocument.Manager = "Self";

 Application.ActiveDocument.Title = "Zeeshan";

 Application.ActiveDocument.Subject = "Visio Diagram";


{{< /highlight >}}
## **Aspose.Diagram**
{{% alert color="primary" %}} 

Microsoft Visio 允许您定义许多文档摘要信息属性，以帮助您和您的同事识别 diagram。摘要属性，例如标题、主题、作者和描述，使文件在搜索时更容易找到，在浏览时更容易识别文件。

{{% /alert %}} 
### **写作 Microsoft Visio 文档摘要信息**
这[文档属性](https://reference.aspose.com/diagram/net/aspose.diagram/documentproperties)类公开了一些属性来设置或获取 Microsoft Visio diagram 的摘要信息。 Aspose.Diagram for .NET 可以更新图纸汇总信息，然后将图纸文件写回VDX。

要更新现有 VDX 或 VSD 文件的图纸摘要信息：

1. 创建一个实例[Diagram](https://reference.aspose.com/diagram/net/aspose.diagram/diagram)班级。
1. 设置 Diagram.DocumentProps 公开的属性以定义 Visio 绘图文件的摘要信息。
1. 调用Diagram类的Save方法将Visio绘图文件写入VDX。

查看摘要信息：

1. 在Microsoft Visio打开输出VDX文件。
1. 选择**信息**来自**文件**菜单。

{{< highlight "cs" >}}

  //Call the diagram constructor to load diagram from a VDX file

 Diagram vdxDiagram = new Diagram("Drawing1.vdx");

 //Set some summary information about the diagram

 vdxDiagram.DocumentProps.Creator = "Ijaz";

 vdxDiagram.DocumentProps.Company = "Aspose";

 vdxDiagram.DocumentProps.Category = "Drawing 2D";

 vdxDiagram.DocumentProps.Manager = "Sergey Polshkov";

 vdxDiagram.DocumentProps.Title = "Aspose Title";

 vdxDiagram.DocumentProps.TimeCreated = DateTime.Now;

 vdxDiagram.DocumentProps.Subject = "Visio Diagram";

 vdxDiagram.DocumentProps.Template = "Aspose Template";

 //Write the updated file to the disk in VDX file format

 vdxDiagram.Save("output.vdx", SaveFileFormat.VDX);


{{< /highlight >}}
## **下载示例代码**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **下载运行代码**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Writing%20Document%20Summary)
