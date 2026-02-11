---
title: Change Layer Properties
type: docs
weight: 130
url: /net/change-properties-layer/
description: This section explains how to change layer's properties with Aspose.Diagram.
---

## **Change Layer Properties in Visio**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) allows to change layer's properties in Microsoft Office Visio diagram.Each shape can belong to multiple layers so developers can change layer's properties to suit end user needs. The [PageSheet](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) class object offers Layers which allows to add and remove layer objects in Visio drawing. Users can manage [Layer](https://reference.aspose.com/diagram/net/aspose.diagram/layer) properties programmatically using Aspose.Diagram API as follows:
### **Change Layer Properties Programming Sample**
The following piece of code helps to change layer's properties.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Layers();

// Load a source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");

// Iterate through the layers
foreach (Aspose.Diagram.Layer layer in Page.PageSheet.Layers)
{
    layer.Visible.Value = Aspose.Diagram.BOOL.True;
    layer.Print.Value = Aspose.Diagram.BOOL.True;
}
// Save diagram
diagram.Save(dataDir + "ChangeLayerProperty_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```