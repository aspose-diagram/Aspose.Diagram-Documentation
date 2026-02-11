---
title: Apply Theme To Shape
type: docs
weight: 70
url: /net/apply-theme-to-shape/
description: This section explains how to set theme Properties in a visio shape with Aspose.Diagram.
---

## **Set Theme Color to a Shape in Visio**
This topic elaborates how developers can apply theme color to a shape using Aspose.Diagram for .NET.

The code below shows how to:

1. Load a sample diagram.
1. get a particular page.
1. get a particular shape.
1. set theme of the shape.
1. save diagram
#### **Set Theme to a shape Programming Sample**
Use the following code in your .NET application to set appearance of the connector type shape using Aspose.Diagram for .NET.


{{< highlight csharp >}}
// ExStart:ApplyThemeToNewShape
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-2");

// Add master with stencil file path and master name
string masterName = "Rectangle";
diagram.AddMaster(dataDir + "Basic Shapes.vss", masterName);

// Page indexing starts from 0
int PageIndex = 1;
double width = 2, height = 2, pinX = 4.25, pinY = 4.5;
// Add a new rectangle shape
long rectangleId = diagram.AddShape(pinX, pinY, width, height, masterName, PageIndex);

// Set shape properties 
Shape rectangle = page.Shapes.GetShape(rectangleId);
rectangle.XForm.PinX.Value = 5;
rectangle.XForm.PinY.Value = 5;
rectangle.Type = TypeValue.Shape;
rectangle.Text.Value.Add(new Txt("Aspose Diagram"));

// Apply preset theme clouds to new shape in page "Page-2"
rectangle.PresetTheme = PresetThemeValue.Clouds;
rectangle.PresetThemeVariant = PresetThemeVariantValue.Variant1;
rectangle.PresetThemeQuickStyle = PresetQuickStyleValue.VariantStyle1;

// Apply preset theme bubble to page "Page-3"
Page page3 = diagram.Pages.GetPage("Page-3");
page3.PresetTheme = PresetThemeValue.Bubble;
page3.PresetThemeVariant = PresetThemeVariantValue.Variant2;
page3.PresetThemeQuickStyle = PresetQuickStyleValue.VariantStyle3;

diagram.Save(dataDir + "ApplyThemeToNewShape_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

