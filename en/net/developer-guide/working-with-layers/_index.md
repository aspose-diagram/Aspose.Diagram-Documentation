---
title: Working with Layers
type: docs
weight: 130
url: /net/working-with-layers/
description: This section explains how to add or get layer information in a visio shape with Aspose.Diagram.
---

## **Configure Shape Objects with Layers in Visio**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) allows to configure shape objects with layers in Microsoft Office Visio diagram. Each shape can belong to multiple layers so developers can manage shapes to suit end user needs. The [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class object offers LayerMember property which allows to add and remove shape objects to and from the layers in Visio drawing. Users can manage these properties programmatically using Aspose.Diagram API as follows:
### **Configure Shape Objects Programming Sample**
The following piece of code helps to add, remove and move shape object properties.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Layers();

// Load a source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");

// Iterate through the shapes
foreach (Aspose.Diagram.Shape shape in page.Shapes)
{
    if (shape.Name.ToLower() == "shape1")
    {
        // Add shape1 in first two layers. Here "0;1" are indexes of the layers
        LayerMem layer = shape.LayerMem;
        layer.LayerMember.Value = "0;1";
    }
    else if (shape.Name.ToLower() == "shape2")
    {
        // Remove shape2 from all the layers
        LayerMem layer = shape.LayerMem;
        layer.LayerMember.Value = "";
    }
    else if (shape.Name.ToLower() == "shape3")
    {
        // Add shape3 in first layer. Here "0" is index of the first layer
        LayerMem layer = shape.LayerMem;
        layer.LayerMember.Value = "0";
    }
}
// Save diagram
diagram.Save(dataDir + "ConfigureShapeLayers_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Add a new Layer in the Visio Diagram**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) allows developers to add new layers to organize custom categories of shapes, and then assign shapes to those layers programmatically. The [LayerCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/layercollection) class offers Add method which allows to add a new [Layer](http://www.aspose.com/api/net/diagram/aspose.diagram/layer) in the Visio drawing. Developers can set Layer properties by initializing its class object.
### **Add Layer Programming Sample**
The following piece of code helps to add Layer objects.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Layers();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// Initialize a new Layer class object
Layer layer = new Layer();
// Set Layer name
layer.Name.Value = "Layer1";
// Set Layer Visibility
layer.Visible.Value = BOOL.True;
// Set the color checkbox of Layer
layer.IsColorChecked = BOOL.True;
// Add Layer to the particular page sheet
page.PageSheet.Layers.Add(layer);

// Get shape by ID
Shape shape = page.Shapes.GetShape(3);
// Assign shape to this new Layer
shape.LayerMem.LayerMember.Value = layer.IX.ToString();
// Save diagram
diagram.Save(dataDir + "AddLayer_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Retrieve All Layers from the Visio Diagram**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) gives access to developers to get the existing layers of a Visio diagram. The [PageSheet](http://www.aspose.com/api/net/diagram/aspose.diagram/pagesheet) property of the [Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class allows to retrieve the list of available layers from a Visio diagram using [LayerCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/layercollection) class.
### **Retrieve Layers Programming Sample**
The following piece of code helps to get the list of Layers.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Layers();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// Iterate through the layers
foreach (Layer layer in page.PageSheet.Layers)
{
    Console.WriteLine("Name: " + layer.Name.Value);
    Console.WriteLine("Visibility: " + layer.Visible.Value);
    Console.WriteLine("Status: " + layer.Status.Value);
}

{{< /highlight >}}
```
