---
title: Group, Convert and Verify Shapes
type: docs
weight: 80
url: /net/group-convert-and-verify-shapes/
description: This section explains how to group shapes with Aspose.Diagram.
---

## **Group Multiple Shapes Together in the Visio Drawing**
Aspose.Diagram API allows developers in grouping shapes together to move them all at once. Each shape in a group maintains a unique identity and has its own set of properties. When we change the formatting of a group of shapes, it assigns the new property to each shape.
### **How to Group Shapes**
The Group method exposed by the [ShapeCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/shapecollection) class can be used to group shapes together.

The code below shows how to:

1. Load a sample diagram.
1. initialized an array of the shapes
1. get a particular shape by id.
1. get another particular particular shape by id.
1. assign shapes to the array.
1. group shapes by calling the Group method.
1. save diagram
#### **Group Shapes Programming Sample**
Use the following code in your .NET application to group shapes together using Aspose.Diagram for .NET API.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

// Initialize an array of shapes
Aspose.Diagram.Shape[] ss = new Aspose.Diagram.Shape[3];

// Extract and assign shapes to the array
ss[0] = page.Shapes.GetShape(15);
ss[1] = page.Shapes.GetShape(16);
ss[2] = page.Shapes.GetShape(17);

// Mark array shapes as group
page.Shapes.Group(ss);

// Save visio diagram
diagram.Save(dataDir + "GroupShapes_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Convert a Visio Shape to Other File Formats**
Aspose.Diagram for .NET API allows developers to convert a single Visio shape to any other supported file format. In this article, we remove all other Visio shapes from the page and customize page setting according to the source Shape size. 
### **Converting a Particular Visio Shape**
Developers can convert a Visio shape to PDF, HTML, Image, SVG, and SWF by **specifying the Visio save options**.
This example code work as follows:

1. Load a source Visio.
1. Get a particular page.
1. Remove the background page.
1. Build a hash table of all shapes holding the ids and names.
1. Iterate through the hash table
1. Remove all shapes from the Visio page, except the particular one.
1. Set the page size.
1. Save the Visio page in any supported file format.
#### **Convert Shape Programming Sample**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram srcVisio = new Diagram(dataDir + "Drawing1.vsdx");

double shapeWidth = 0;
double shapeHeight = 0;

// Get Visio page
Aspose.Diagram.Page srcPage = srcVisio.Pages.GetPage("Page-3");
// Remove background page
srcPage.BackPage = null;

// Get hash table of shapes, it holds id and name
Hashtable remShapes = new Hashtable();
// Hashtable<Long, String> remShapes = new Hashtable<Long, String>();
foreach (Aspose.Diagram.Shape shape in srcPage.Shapes)
    // For the normal shape
    remShapes.Add(shape.ID, shape.Name);

// Iterate through the hash table
foreach (DictionaryEntry shapeEntry in remShapes)
{
    long key = (long)shapeEntry.Key;
    string val = (string)shapeEntry.Value;
    Aspose.Diagram.Shape shape = srcPage.Shapes.GetShape(key);
    // Check of the shape name
    if (val.Equals("GroupShape1"))
    {
        // Move shape to the origin corner
        shapeWidth = shape.XForm.Width.Value;
        shapeHeight = shape.XForm.Height.Value;
        shape.MoveTo(shapeWidth * 0.5, shapeHeight * 0.5);
        // Trim page size
        srcPage.PageSheet.PageProps.PageWidth.Value = shapeWidth;
        srcPage.PageSheet.PageProps.PageHeight.Value = shapeHeight;
    }
    else
    {
        // Remove shape from the Visio page and hash table
        srcPage.Shapes.Remove(shape);
    }
}
remShapes.Clear();

// Specify saving options
Aspose.Diagram.Saving.PdfSaveOptions opts = new Aspose.Diagram.Saving.PdfSaveOptions();
// Set page count to save
opts.PageCount = 1;
// Set starting index of the page
opts.PageIndex = 1;
// Save it
srcVisio.Save(dataDir + "SaveVisioShapeInOtherFormats_out.pdf", opts);

{{< /highlight >}}
```
### **Convert Visio Shape to PDF**
The ToPdf method of the Shape class allows to convert a shape into the PDF format.

{{< highlight java >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// save a shape in the PDF format

diagram.Pages[0].Shapes.GetShape(59).ToPdf(dataDir + "out.pdf");

{{< /highlight >}}
### **Convert Visio Shape to HTML**
The ToHTML method of the Shape class allows to convert a shape into the HTML format.

{{< highlight java >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Aspose.Diagram.Saving.HTMLSaveOptions hs = new Aspose.Diagram.Saving.HTMLSaveOptions();

// save a shape in the PDF format

diagram.Pages[0].Shapes.GetShape(59).ToHTML(dataDir + "out.pdf", hs);

{{< /highlight >}}
## **Verify Whether Two Visio Shapes are Connected or Glued**
Aspose.Diagram for .NET API allows developers to verify that the two Visio shapes are glued or connected. Previously, we have seen that how we can connect or glue two shapes in these help topics: [Add and Connect Visio Shapes](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/) and [Glue Shapes Inside the Container](/diagram/net/working-with-shapes-gluing/).
### **Verification of the Connected or Glued Shapes**
The [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class offers IsGlued and IsConnected properties to determine whether two shapes are glued or connected.
#### **Verification of Connected or Glued Shapes Programming Sample**
The following piece of code verifies whether two shapes are connected or glued.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Set two shape ids
long ShapeIdOne = 15;
long ShapeIdTwo = 16;

// Get Visio page by name
Page page = diagram.Pages.GetPage("Page-3");

// Get Visio shapes by ids
Shape ShapedOne = page.Shapes.GetShape(ShapeIdOne);
Shape ShapedTwo = page.Shapes.GetShape(ShapeIdTwo);

// Determine whether shapes are connected
bool connected = ShapedOne.IsConnected(ShapedTwo);
Console.WriteLine("Shapes are connected: " + connected);

// Determine whether shapes are glued
bool glued = ShapedOne.IsGlued(ShapedTwo);
Console.WriteLine("Shapes are Glued: " + glued);

{{< /highlight >}}
```
## **Verify Whether the Visio Shape is in a Group of Shapes**
Aspose.Diagram for .NET API allows developers to verify that the Visio shape is in a group of shapes or not.
### **Verification of Shape in the Group of Shapes**
The [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class offers IsInGroup properties to determine whether the Visio shape is in a group shape.
#### **Verification of Shape in the Group of Shapes Programming Sample**
The following piece of code verifies whether the shape is in a group shape.

```
{{< highlight "csharp" >}}
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();
// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a sub-shape by page name, group shape ID, and then sub-shape ID
Shape shape = diagram.Pages.GetPage("Page-3").Shapes.GetShape(13).Shapes.GetShape(2);
Console.WriteLine("Is it in a Group: " + shape.IsInGroup());
{{< /highlight >}}
```
