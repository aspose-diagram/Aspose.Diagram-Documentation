---
title: Add Watermark to Visio
type: docs
weight: 10
url: /net/add-watermark-to-visio/
keywords: "watermark, visio"
description: How to add watermark to visio using .NET Diagram API.
---

## **Creating a Diagram**
Aspose.Diagram for .NET lets you read and create Microsoft Visio diagrams from within your own applications, without Microsoft Office Automation. The first step when creating new documents, is to create a diagram. Then [add shapes and connectors](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/) to build up the diagram. Use the default constructor of [Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class to create a new diagram.
### **Programming Sample**
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

This example work as follows:

1. Create an object of the Diagram class.
1. Add watermark to visio in page
1. Call Save method of the Diagram class object and also pass complete file path and the DiagramSaveOptions object.
### **Add watermark Programming Sample**
The following example code shows how to add watermark in the Visio diagram.

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
