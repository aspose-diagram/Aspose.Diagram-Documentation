---
title: Create, Update, Layout and Auto-Fit Shapes
type: docs
weight: 10
url: /net/create-update-layout-and-auto-fit-shapes/
description: Use C# Diagram API to create, update and auto layout shapes in Visio files using C# within your applications. Complete guide with C# code samples.
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

## **Layout Shapes in Flowchart Style**
With certain types of connected drawings, such as flowcharts and network diagrams, you can use the **Layout Shapes** feature to automatically position shapes. Automatically positioning is faster than manually dragging each shape to a new location.

For example, if you're updating a large flowchart to include a new process, you can add and connect the shapes that make up the process, and then use the layout feature to automatically layout the updated drawing.

The Layout method, exposed by the [Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class layouts the shapes and/or reroutes the connectors on all the diagram's pages. This method accepts an [LayoutOptions](https://reference.aspose.com/diagram/net/aspose.diagram.autolayout/layoutoptions) object as an argument. Use the different properties exposed by the LayoutOptions class to automatically layout shapes.

The image below shows the diagram loaded by the code snippets in this article, before auto layout is applied. The code snippets show how to apply [flowchart layouts](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/) and [compact tree layouts](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/).

**The source diagram.**

![todo:image_alt_text](create-update-layout-and-auto-fit-shapes_1.png)

The code snippets in this article takes the source diagram and applies several types of auto layout to it, saving each in a separate file.

|<p>**Layout shapes bottom to top** </p><p>![todo:image_alt_text](create-update-layout-and-auto-fit-shapes_2.png)</p>|<p>**Layout shapes top to bottom** </p><p>![todo:image_alt_text](create-update-layout-and-auto-fit-shapes_3.png)</p>|
| :- | :- |
|<p>**Layout shapes left to right** </p><p>![todo:image_alt_text](create-update-layout-and-auto-fit-shapes_4.png)</p>|<p>**Layout shapes right to left** </p><p>![todo:image_alt_text](create-update-layout-and-auto-fit-shapes_5.png)</p>|
To layout shapes in flowchart style:

1. Create an instance of the Diagram class.
1. Create an instance of LayoutOptions class and set Flowchart style related properties.
1. Call the Diagram class' Layout method by passing LayoutOptions.
1. Call the Diagram class' Save method to write the Visio drawing.
### **Flowchart Style Programming Sample**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Load an existing Visio diagram
string fileName = "LayOutShapesInFlowchartStyle.vdx";
Diagram diagram = new Diagram(dataDir + fileName);

// Set layout options 
LayoutOptions flowChartOptions = new LayoutOptions();
flowChartOptions.LayoutStyle = LayoutStyle.FlowChart;
flowChartOptions.SpaceShapes = 1f;
flowChartOptions.EnlargePage = true;

// Set layout direction as BottomToTop and then save
flowChartOptions.Direction = LayoutDirection.BottomToTop;
diagram.Layout(flowChartOptions);
diagram.Save(dataDir + "sample_btm_top_out.vdx", SaveFileFormat.VDX);

// Set layout direction as TopToBottom and then save
diagram = new Diagram(dataDir + fileName);
flowChartOptions.Direction = LayoutDirection.TopToBottom;
diagram.Layout(flowChartOptions);
diagram.Save(dataDir + "sample_top_btm_out.vdx", SaveFileFormat.VDX);

// Set layout direction as LeftToRight and then save
diagram = new Diagram(dataDir + fileName);
flowChartOptions.Direction = LayoutDirection.LeftToRight;
diagram.Layout(flowChartOptions);
diagram.Save(dataDir + "sample_left_right_out.vdx", SaveFileFormat.VDX);

// Set layout direction as RightToLeft and then save
diagram = new Diagram(dataDir + fileName);
flowChartOptions.Direction = LayoutDirection.RightToLeft;
diagram.Layout(flowChartOptions);
diagram.Save(dataDir + "sample_right_left_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}

### **Laying Out Shapes in the Compact Tree Style**
The compact tree layout style tries to built a tree structure. It uses the same input file as the [example above](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/) and saves out to several different compact tree styles.

|<p>**Compact tree layout - down and right** </p><p>![todo:image_alt_text](create-update-layout-and-auto-fit-shapes_6.png)</p>|
| :- |
|<p>**Compact tree layout - down and left** </p><p>![todo:image_alt_text](create-update-layout-and-auto-fit-shapes_7.png)</p>|


|<p>**Compact tree layout - right and down** </p><p>![todo:image_alt_text](create-update-layout-and-auto-fit-shapes_8.png)</p>|<p>**Compact tree layout - left and down** </p><p>![todo:image_alt_text](create-update-layout-and-auto-fit-shapes_9.png)</p>|
| :- | :- |
To layout shapes in the compact tree style:

1. Create an instance of the [Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class.
1. Create an instance of the LayoutOptions class and set compact tree style properties.
1. Call the Diagram class' Layout method by passing LayoutOptions.
1. Call the the Diagram class' Save method to write the Visio file.
#### **Compact Tree Style Programming Sample**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

string fileName = "LayOutShapesInCompactTreeStyle.vdx";
// Load an existing Visio diagram
Diagram diagram = new Diagram(dataDir + fileName);

// Set layout options 
LayoutOptions compactTreeOptions = new LayoutOptions();
compactTreeOptions.LayoutStyle = LayoutStyle.CompactTree;
compactTreeOptions.EnlargePage = true;

// Set layout direction as DownThenRight and then save
compactTreeOptions.Direction = LayoutDirection.DownThenRight;
diagram.Layout(compactTreeOptions);
diagram.Save(dataDir + "sample_down_right.vdx", SaveFileFormat.VDX);

// Set layout direction as DownThenLeft and then save
diagram = new Diagram(dataDir + fileName);
compactTreeOptions.Direction = LayoutDirection.DownThenLeft;
diagram.Layout(compactTreeOptions);
diagram.Save(dataDir + "sample_down_left.vdx", SaveFileFormat.VDX);

// Set layout direction as RightThenDown and then save
diagram = new Diagram(dataDir + fileName);
compactTreeOptions.Direction = LayoutDirection.RightThenDown;
diagram.Layout(compactTreeOptions);
diagram.Save(dataDir + "sample_right_down.vdx", SaveFileFormat.VDX);

// Set layout direction as LeftThenDown and then save
diagram = new Diagram(dataDir + fileName);
compactTreeOptions.Direction = LayoutDirection.LeftThenDown;
diagram.Layout(compactTreeOptions);
diagram.Save(dataDir + "sample_left_down.vdx", SaveFileFormat.VDX);

{{< /highlight >}}

## **Auto-fit the Visio Diagram**
Aspose.Diagram API supports auto-fitting of the Visio drawing. This feature operation helps to bring outside shapes inside the Visio page boundary. Aspose.Diagram for .NET API has the [Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class that represents a Visio drawing. The [DiagramSaveOptions](https://reference.aspose.com/diagram/net/aspose.diagram.saving/diagramsaveoptions) class exposes AutoFitPageToDrawingContent property to auto fit the Visio drawing.

This example work as follows:

1. Create an object of the Diagram class.
1. Create an object of the DiagramSaveOptions class and pass the resultant file format.
1. Set AutoFitPageToDrawingContent property of the DiagramSaveOptions object.
1. Call Save method of the Diagram class object and also pass complete file path and the DiagramSaveOptions object.
### **Auto-fit Programming Sample**
The following example code shows how to auto-fit shapes in the Visio diagram.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "BFlowcht.vsdx");

// Use saving options
DiagramSaveOptions options = new DiagramSaveOptions(SaveFileFormat.VSDX);
// Set Auto fit page property
options.AutoFitPageToDrawingContent = true;

// Save Visio diagram
diagram.Save(dataDir + "AutoFitShapesInVisio_out.vsdx", options);

{{< /highlight >}}

## **Working with VBA Project**
### **Modify VBA Module Code in Visio Diagram**
This article demonstrates how to modify a VBA module code automatically using Aspose.Diagram for .NET. We have added [VbaModule](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaModule), [VbaModuleCollection](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaModuleCollection), [VbaProject](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProject), [VbaProjectReference](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProjectReference) and [VbaProjectReferenceCollection](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProjectReferenceCollection) classes. These classes help to get control over VBA project. Developers can extract and modify VBA module code.
### **Modify VBA Module Code Programming Sample**
Please check this code example:


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Load an existing Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdm", LoadFileFormat.VSDM);
// Extract VBA project
Aspose.Diagram.Vba.VbaProject v = diagram.VbaProject;
// Iterate through the modules and modify VBA module code
foreach (VbaModule module in diagram.VbaProject.Modules)
{
    string code = module.Codes;
    if (code.Contains("This is test message."))
        code = code.Replace("This is test message.", "This is Aspose.Diagram message.");
    module.Codes = code;
}
// Save the Visio diagram
diagram.Save(dataDir + "ModifyVBAModule_out.vssm", SaveFileFormat.VSSM);

{{< /highlight >}}

### **Remove All Macros from the Visio Diagram**
Aspose.Diagram for .NET allows developers to remove all macros from the Visio diagram. The VbProjectData property, exposed by the [Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class, allows you to remove all macros from the Visio drawing.
### **Remove All Macros Programming Sample**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Remove all macros
diagram.VbProjectData = null;

// Save diagram
diagram.Save(dataDir + "RemoveMacrosFromVisio_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Creating a New Diagram with VSTO**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) lets developers to create and work with Microsoft Office Visio diagrams and incorporate features in their software applications. There are other ways of working with Visio files, most commonly, Microsoft Automation. Unfortunately, that has some limitations. Aspose.Diagram is powerful and fast and works independently without Microsoft Office installation.

This migration article shows how to use first [VSTO](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/) and then [Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) to create a new diagram and add some shapes to it. You'll notice that the Aspose.Diagram code is shorter than VSTO code. Feel free to use the code as a base for your own development and enhance it to meet your needs. VSTO lets you program with Microsoft Visio files. To create a new diagram:

1. Create a Visio application object.
1. Make the application object invisible.
1. Create an empty diagram.
1. Add shapes from Visio masters (stencils).
1. Save the file as VDX.
### **Create New Diagram with VSTO Programming Sample**
{{% alert color="primary" %}}

using Visio = Microsoft.Office.Interop.Visio;
Imports Visio = Microsoft.Office.Interop.Visio

{{% /alert %}}


**Example:**


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_KnowledgeBase();

Visio.Application vdxApp = null;
Visio.Document vdxDoc = null;
try
{
    // Create Visio Application Object
    vdxApp = new Visio.Application();

    // Make Visio Application Invisible
    vdxApp.Visible = false;

    // Create a new diagram
    vdxDoc = vdxApp.Documents.Add("");

    // Load Visio Stencil
    Visio.Documents visioDocs = vdxApp.Documents;
    Visio.Document visioStencil = visioDocs.OpenEx("Basic Shapes.vss",
        (short)Microsoft.Office.Interop.Visio.VisOpenSaveArgs.visOpenHidden);

    // Set active page
    Visio.Page visioPage = vdxApp.ActivePage;

    // Add a new rectangle shape
    Visio.Master visioRectMaster = visioStencil.Masters.get_ItemU(@"Rectangle");
    Visio.Shape visioRectShape = visioPage.Drop(visioRectMaster, 4.25, 5.5);
    visioRectShape.Text = @"Rectangle text.";

    // Add a new star shape
    Visio.Master visioStarMaster = visioStencil.Masters.get_ItemU(@"Star 7");
    Visio.Shape visioStarShape = visioPage.Drop(visioStarMaster, 2.0, 5.5);
    visioStarShape.Text = @"Star text.";

    // Add a new hexagon shape
    Visio.Master visioHexagonMaster = visioStencil.Masters.get_ItemU(@"Hexagon");
    Visio.Shape visioHexagonShape = visioPage.Drop(visioHexagonMaster, 7.0, 5.5);
    visioHexagonShape.Text = @"Hexagon text.";


    // Save diagram as VDX
    vdxDoc.SaveAs(dataDir + "CreatingDiagramWithVSTO_out.vdx");
}
catch (Exception ex)
{
    Console.WriteLine(ex.Message + "\nThis example will only work if you apply a valid Aspose License. You can purchase full license or get 30 day temporary license from http:// Www.aspose.com/purchase/default.aspx.");
}
            

{{< /highlight >}}

## **Creating a New Diagram with Aspose.Diagram for .NET**
Using Aspose.Diagram API, developers don't need Microsoft Office Visio installation on the machine, and they can work independently of Microsoft Office Automation.

To create a new diagram:

1. Create an empty diagram.
1. Add shapes from Visio masters (stencils).
1. Save the file as VDX.
### **New Diagram with Aspose.Diagram for .NET Programming Sample**
{{% alert color="primary" %}}

using Aspose.Diagram;
Imports Aspose.Diagram

{{% /alert %}}

Example:


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_KnowledgeBase();

// Create a new diagram
Diagram diagram = new Diagram(dataDir + "Basic Shapes.vss");

// Add a new rectangle shape
long shapeId = diagram.AddShape(4.25, 5.5, 2, 1, @"Rectangle", 0);
Shape shape = diagram.Pages[0].Shapes.GetShape(shapeId);
shape.Text.Value.Add(new Txt(@"Rectangle text."));

// Add a new star shape
shapeId = diagram.AddShape(2.0, 5.5, 2, 2, @"Star 7", 0);
shape = diagram.Pages[0].Shapes.GetShape(shapeId);
shape.Text.Value.Add(new Txt(@"Star text."));

// Add a new hexagon shape
shapeId = diagram.AddShape(7.0, 5.5, 2, 2, @"Hexagon", 0);
shape = diagram.Pages[0].Shapes.GetShape(shapeId);
shape.Text.Value.Add(new Txt(@"Hexagon text."));

// Save the new diagram
diagram.Save(dataDir + "CreatingDiagramWithAspose_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}

## **Update Shape Properties**
When working with Microsoft Visio diagrams, users can update shape attributes including text, style, position, height and width. As a software developer working with Visio files, you'll be asked to do this programmatically. The good news is that it is possible, either using the mechanisms for programming with Visio files that Microsoft provides, VSTO, or using [Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).

Below topic shows how to use [VSTO](https://products.aspose.com/diagram/net/) and [Aspose.Diagram](https://products.aspose.com/diagram/net/) to update shape properties. The code snippets below show how to update shape properties for VSTO and Aspose.Diagram for .NET. Feel free to use the code and apply it to your particular situation.
### **Updating Shape Properties with VSTO**
VSTO lets you program with Microsoft Visio files. To update shape properties:

1. Create a Visio application object.
1. Make the application object invisible.
1. Open an existing Visio VSD file.
1. Find the required shape.
1. Update the shape properties (text, text style, position and size).
1. Save the file as VDX.
#### **Updating Shape Properties with VSTO Programming Sample**
{{% alert color="primary" %}}

using Visio = Microsoft.Office.Interop.Visio;
Imports Visio = Microsoft.Office.Interop.Visio

{{% /alert %}}

**Example:**


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_KnowledgeBase();

Visio.Application vsdApp = null;
Visio.Document vsdDoc = null;
try
{
    // Create Visio Application Object
    vsdApp = new Visio.Application();

    // Make Visio Application Invisible
    vsdApp.Visible = false;

    // Create a document object and load a diagram
    vsdDoc = vsdApp.Documents.Open(dataDir + "Drawing1.vsd");

    // Create page object to get required page
    Visio.Page page = vsdApp.ActivePage;

    // Create shape object to get required shape
    Visio.Shape shape = page.Shapes["Process1"];

    // Set shape text and text style
    shape.Text = "Hello World";
    shape.TextStyle = "CustomStyle1";

    // Set shape's position
    shape.get_Cells("PinX").ResultIU = 5;
    shape.get_Cells("PinY").ResultIU = 5;

    // Set shape's height and width
    shape.get_Cells("Height").ResultIU = 2;
    shape.get_Cells("Width").ResultIU = 3;

    // Save file as VDX
    vsdDoc.SaveAs(dataDir + "Drawing1.vdx");
}
catch (Exception ex)
{
    Console.WriteLine(ex.Message + "\nThis example will only work if you apply a valid Aspose License. You can purchase full license or get 30 day temporary license from http:// Www.aspose.com/purchase/default.aspx.");
}           

{{< /highlight >}}

### **Updating Shape Properties with Aspose.Diagram for .NET**
Using Aspose.Diagram API, developers don't need Microsoft Office Visio on the machine, and they can work independently of Microsoft Office Automation.

To update shape properties with Aspose.Diagram for .NET:

1. Open an existing Visio VSD file.
1. Find the required shape.
1. Update the shape properties (text, text style, position and size).
1. Save the file as VDX.
#### **Updating Shape Properties with Aspose.Diagram for .NET Programming Sample**
{{% alert color="primary" %}}

using Aspose.Diagram;
Imports Aspose.Diagram

{{% /alert %}}

**Example:**


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
try
{
    // The path to the documents directory.
    string dataDir = RunExamples.GetDataDir_KnowledgeBase();

    // Save the uploaded file as PDF
    Diagram diagram = new Diagram(dataDir + "Drawing1.vsd");

    // Find a particular shape and update its properties
    foreach (Aspose.Diagram.Shape shape in diagram.Pages[0].Shapes)
    {
        if (shape.Name.ToLower() == "process1")
        {
            shape.Text.Value.Clear();
            shape.Text.Value.Add(new Txt("Hello World"));

            // Find custom style sheet and set as shape's text style
            foreach (StyleSheet styleSheet in diagram.StyleSheets)
            {
                if (styleSheet.Name == "CustomStyle1")
                {
                    shape.TextStyle = styleSheet;
                }
            }

            // Set horizontal and vertical position of the shape
            shape.XForm.PinX.Value = 5;
            shape.XForm.PinY.Value = 5;

            // Set height and width of the shape
            shape.XForm.Height.Value = 2;
            shape.XForm.Width.Value = 3;
        }
    }

    // Save shape as VDX
    diagram.Save(dataDir + "UpdateShapePropsWithAspose_out.vdx", SaveFileFormat.VDX);
}
catch (Exception ex)
{
    Console.WriteLine(ex.Message);
}

{{< /highlight >}}

