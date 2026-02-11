---
title: Visio加水印
type: docs
weight: 10
url: /zh/net/add-watermark-to-visio/
keywords: watermark, visi
description: 如何使用 .NET Diagram API 为 visio 添加水印。
---
## **创建一个 Diagram**
 Aspose.Diagram for .NET 允许您从自己的应用程序中读取和创建 Microsoft Visio 图表，无需 Microsoft Office 自动化。创建新文档的第一步是创建一个 diagram。然后[添加形状和连接器](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/)构建 diagram。使用默认构造函数[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)类创建一个新的 diagram。
### **编程范例**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Create directory if it is not already present.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// Initialize a new Visio
Diagram diagram = new Diagram();
dataDir = dataDir + "CreateDiagram_out.vsdx";
// Save in the VSDX format
diagram.Save(dataDir, SaveFileFormat.VSDX);

{{< /highlight >}}
```

这个例子的工作原理如下：

1. 创建 Diagram 类的对象。
1. 页面中visio加水印
1. 调用 Diagram 类对象的 Save 方法，并传递完整的文件路径和 DiagramSaveOptions 对象。
### **添加水印编程示例**
下面的示例代码展示了如何在 Visio diagram 中添加水印。

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
static string text = "";
public static void Run()
{
    // The path to the documents directory.
    string dataDir = RunExamples.GetDataDir_ShapeText();
    // Load diagram
    Diagram diagram = new Diagram(dataDir + "Drawing1.vsd");

    // Get Visio diagram page
    Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

    double pinx = page.PageSheet.PageProps.PageWidth.Value / 2;
    double piny = page.PageSheet.PageProps.PageHeight.Value / 2;
    double width = page.PageSheet.PageProps.PageWidth.Value;
    double height = page.PageSheet.PageProps.PageHeight.Value;
    
    //Add watermark
    Shape shape = page.AddText(pinx, piny, width, height, "Test text","Calibri","#a5a5a5",0.25);
    diagram.Save(dataDir + "Watermark.vsdx", SaveFileFormat.VSDX);
}


{{< /highlight >}}
```
