---
title: Rotate Visio Shape Text
type: docs
weight: 9
url: /net/rotate-visio-shape-text/
keywords: "Rotate, visio, Text"
description: How to rotate shape's text in visio using .NET Diagram API.
---

## **Creating a Diagram**
Aspose.Diagram for .NET lets you read and create Microsoft Visio diagrams from within your own applications, without Microsoft Office Automation. The first step when creating new documents, is to create a diagram. Then [add shapes and connectors](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/) to build up the diagram. Use the default constructor of [Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class to create a new diagram.
### **Programming Sample**

{{< highlight csharp >}}
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


This example work as follows:

1. Create an object of the Diagram class.
1. Get paticular page
1. Get paticular shape
1. Get Shape text and rotate the text
1. Call Save method of the Diagram class object and also pass complete file path and the DiagramSaveOptions object.
### **Rotate text Programming Sample**
The following example code shows how to rotate text in the Visio diagram.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeText();

// Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir + "UpdateShapeText.vsd");
// Get page by name
Page page = diagram.Pages.GetPage("Flow 1");
// Find a particular shape and update its text
foreach (Aspose.Diagram.Shape shape in page.Shapes)
{
    if (shape.NameU.ToLower() == "process" && shape.ID == 1)
    {
        shape.Text.Value.Clear();
        shape.Text.Value.Add(new Txt("New Text"));
        // Set orientation angle
        double angleDeg = 90;
        double angleRad = (Math.PI / 180) * angleDeg;
        shape.TextXForm.TxtAngle.Value = angleRad;
    }
}
// Save diagram
diagram.Save(dataDir + "UpdateShapeText_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}

