---
title: 将 VSD 文件保存为不同的文件格式
type: docs
weight: 10
url: /zh/net/save-vsd-file-to-different-file-formats/
---
In this article, we compare the conversion features of Aspose.Diagram for .NET with VSTO. It contains .NET code samples to convert VSD files to VDX, PDF, and JPEG file formats.
## **VSTO**
VSTO 允许您使用 Microsoft Visio 文件进行编程。要将文件保存为其他格式：

1. 创建一个 Visio 应用程序对象。
1. 使应用程序对象不可见。
1. 加载 diagram。
1. Save to VDX, PDF, and JPEG.
1. 退出 Visio 应用程序对象。

{{< highlight "csharp" >}}

 //Create Visio Application Object

Visio.Application vsdApp = Application;

//Make Visio Application Invisible

vsdApp.Visible = false;

//Create a document object and load a diagram

Visio.Document vsdDoc = vsdApp.Documents.Open("Drawing.vsd");

//Save the VDX diagram

vsdDoc.SaveAs("Drawing1.vdx");

//Save as PDF file

vsdDoc.ExportAsFixedFormat(Visio.VisFixedFormatTypes.visFixedFormatPDF,

	"Drawing1.pdf", Visio.VisDocExIntent.visDocExIntentScreen,

	Visio.VisPrintOutRange.visPrintAll, 1, vsdDoc.Pages.Count, false, true,

	true, true, true, System.Reflection.Missing.Value);

Visio.Page vsdPage = vsdDoc.Pages[1];

//Save as JPEG Image

vsdPage.Export("Drawing1.jpg");

//Quit Visio Object

vsdApp.Quit();

{{< /highlight >}}
## **Aspose.Diagram**
用Aspose.Diagram编程时，机器上不需要Microsoft Visio，可以独立于Microsoft Office自动化工作。下面的代码片段展示了如何：

1. 加载一个 diagram。
1. Save the diagram to VDX, PDF, and JPEG.

{{< highlight "csharp" >}}

 //Load diagram

Diagram vsdDiagram = new Diagram("Drawing.vsd");

//Save the diagram as VDX

vsdDiagram.Save("Drawing1.vdx", SaveFileFormat.VDX);

//Save as PDF

vsdDiagram.Save("Drawing1.pdf", SaveFileFormat.PDF);

//Save as JPEG

vsdDiagram.Save("Drawing1.jpg", SaveFileFormat.JPEG);

{{< /highlight >}}
## **下载示例代码**
- [Github](https://github.com/asposemarketplace/Aspose_for_VSTO/releases/download/Aspose.Diagram1.0/Save.VSD.file.to.different.file.formats.VDX.PDF.and.JPEG.Aspose.Diagram.zip)
- [Sourceforge](https://sourceforge.net/projects/asposevsto/files/Aspose.Diagram%20Vs%20VSTO%20Visio/Save%20VSD%20file%20to%20different%20file%20formats%20VDX%20PDF%20and%20JPEG%20\(Aspose.Diagram\).zip/下载）
- [比特桶](https://bitbucket.org/asposemarketplace/aspose-for-vsto/downloads/Save%20VSD%20file%20to%20different%20file%20formats%20VDX%20PDF%20and%20JPEG%20\(Aspose.Diagram\)。压缩）
