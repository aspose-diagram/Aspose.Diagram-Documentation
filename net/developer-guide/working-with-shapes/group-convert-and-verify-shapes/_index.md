---
title: Group, Convert and Verify Shapes
type: docs
weight: 80
url: /net/group-convert-and-verify-shapes/
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

{{< gist "aspose-diagram" "cce69e51f567ea17ef24bc35fef0f689" "Examples-CSharp-Working-Shapes-GroupShapes-GroupShapes.cs" >}}
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
{{< gist "aspose-diagram" "cce69e51f567ea17ef24bc35fef0f689" "Examples-CSharp-Working-Shapes-SaveVisioShapeInOtherFormats-SaveVisioShapeInOtherFormats.cs" >}}
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

{{< gist "aspose-diagram" "cce69e51f567ea17ef24bc35fef0f689" "Examples-CSharp-Working-Shapes-VerifyConnectedOrGluedShapes-VerifyConnectedOrGluedShapes.cs" >}}
## **Verify Whether the Visio Shape is in a Group of Shapes**
Aspose.Diagram for .NET API allows developers to verify that the Visio shape is in a group of shapes or not.
### **Verification of Shape in the Group of Shapes**
The [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class offers IsInGroup properties to determine whether the Visio shape is in a group shape.
#### **Verification of Shape in the Group of Shapes Programming Sample**
The following piece of code verifies whether the shape is in a group shape.

{{< gist "aspose-diagram" "cce69e51f567ea17ef24bc35fef0f689" "Examples-CSharp-Working-Shapes-VerifyShapeIsInGroup-VerifyShapeIsInGroup.cs" >}}
