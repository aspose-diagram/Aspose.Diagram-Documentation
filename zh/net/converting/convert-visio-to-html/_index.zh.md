---
title: Convert Visio to HTML format 
linktitle: Convert Visio to HTML
type: docs
weight: 30
url: /zh/net/convert-visio-to-html/
description: This topic show you how to Aspose.Diagram allows to convert Visio to html formats. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to html with a few lines of code.
---
## **导出 Visio 到 HTML**
This article explains how to export a Microsoft Visio diagram to HTML using [Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API.

使用[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class constructor to read the diagram files and the Save method to export the diagram to any supported image format. Developers can save resultant HTML in the local storage or directly to a stream instance.

1. [Save resultant HTML in the local storage](https://docs.aspose.com/diagram/net/convert-visio-to-html/#save-resultant-html-in-the-local-storage).
1. [Save resultant HTML in a stream instance](https://docs.aspose.com/diagram/net/convert-visio-to-html/#save-resultant-html-in-a-stream-instance).

The image below shows a VSD file about to be saved to PNG format. You can use other diagram formats (VSDX, VSDM, VSTX, VSSX, VSS, VSSM, VDX, VST, VSTX, VDX, VTX or VSX) as well.

|**输入 diagram。**|
|:- |
|![待办事项：图片_替代_文本](how-to-convert-a-visio-diagram_6.png)|
In order to export VSD diagram to HTML, perform the following steps:

1. 创建 Diagram 类的实例。
1. Call the Dagram class' Save method and set HTML as the output format.
### **Save resultant HTML in the local storage**
生成的文件可以通过传递完整的路径字符串来保存，包括文件名和扩展名，例如@"c:\temp\MyOutput.html"。
#### **Save Resultant HTML in Local Storage Programming Sample**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();
// Load diagram
Diagram diagram = new Diagram(dataDir + "ExportToHTML.vsd");
// Save diagram
diagram.Save(dataDir + "outputVSDtoHTML.html", SaveFileFormat.HTML);

{{< /highlight >}}




### **Save resultant HTML in a stream instance**
It is for use case to save the resultant HTML in a database or repository without storing it in the local storage. This feature also embeds other resultant resources of the HTML, e.g. fonts, CSS (containing the style information) and images. Since it saves a single HTML file into the stream instance.
#### **Save Resultant HTML in a Stream Programming Sample**
{{< highlight "java" >}}

 // Load an existing visio diagram

Diagram diagram = new Diagram("Basic Flowchart.vsd");

// Save resultant HTML directly to a stream

MemoryStream stream = new MemoryStream();

diagram.Save(stream, SaveFileFormat.HTML);



{{< /highlight >}}
