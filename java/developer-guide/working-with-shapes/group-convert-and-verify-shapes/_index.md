---
title: Group, Convert and Verify Shapes
type: docs
weight: 50
url: /java/group-convert-and-verify-shapes/
---

## **Group Multiple Shapes Together in the Visio Drawing**
Aspose.Diagram API allows developers in grouping shapes together to move them all at once. Each shape in a group maintains a unique identity and has its own set of properties. When we change the formatting of a group of shapes, it assigns the new property to each shape.
### **How to Group Shapes**
The Group method exposed by the [ShapeCollection](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shapecollection) class can be used to group shapes together.

The code below shows how to:

1. Load a sample diagram.
1. initialized an array of the shapes
1. get a particular shape by id.
1. get another particular particular shape by id.
1. assign shapes to the array.
1. group shapes by calling the Group method.
1. save diagram
#### **Group Shapes Programming Sample**
Use the following code in your Java application to group shapes together using Aspose.Diagram for Java API.

{{< gist "aspose-diagram" "92a05cb833bad6d60de2968c96b40ee4" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-GroupShapes-GroupShapes.java" >}}
## **Convert a Visio Shape to Other File Formats**
Aspose.Diagram for Java API allows developers to convert a single Visio shape to any other supported file format. In this article, we remove all other Visio shapes from the page and customize page setting according to the source Shape size. 
### **Converting a Particular Visio Shape**
Developers can convert a Visio shape to PDF, HTML, Image, SVG, and SWF by [specifying the Visio save options]().
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
{{< gist "aspose-diagram" "92a05cb833bad6d60de2968c96b40ee4" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-SaveVisioShapeInOtherFormats-SaveVisioShapeInOtherFormats.java" >}}
### **Convert Visio Shape to PDF**
The ToPdf method of the Shape class allows to convert a shape into the PDF format.

{{< highlight java >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toPdf(dataDir + "out.pdf");

{{< /highlight >}}
### **Convert Visio Shape to HTML**
The ToHTML method of the Shape class allows to convert a shape into the HTML format.

{{< highlight java >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

HTMLSaveOptions hs = new HTMLSaveOptions();

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toHTML(dataDir + "out.pdf", hs);

{{< /highlight >}}

{{% alert color="primary" %}} 

We welcome your queries and suggestions at [Aspose.Diagram Forum](https://forum.aspose.com/c/diagram/17). We'll reply promptly.

{{% /alert %}} 
## **Verify Whether Two Visio Shapes are Connected or Glued**
Aspose.Diagram for Java API allows developers to verify that the two Visio shapes are glued or connected. Previously, we have seen that how we can connect or glue two shapes in these help topics: [Add and Connect Visio Shapes](/diagram/java/add-and-connect-visio-shapes/) and [Glue Shapes Inside the Container](/diagram/java/working-with-shapes-gluing/).
### **Verification of the Connected or Glued Shapes**
The [Shape](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shape) class offers IsGlued and IsConnected properties to determine whether two shapes are glued or connected.
#### **Verification of Connected or Glued Shapes Programming Sample**
The following piece of code verifies whether two shapes are connected or glued.

{{< gist "aspose-diagram" "92a05cb833bad6d60de2968c96b40ee4" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-VerifyConnectedOrGluedShapes-VerifyConnectedOrGluedShapes.java" >}}
## **Verify Whether the Visio Shape is in a Group of Shapes**
Aspose.Diagram for Java API allows developers to verify that the Visio shape is in a group of shapes or not.
### **Verification of Shape in the Group of Shapes**
The [Shape](https://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shape) class offers IsInGroup properties to determine whether the Visio shape is in a group shape.
#### **Verification of Shape in the Group of Shapes Programming Sample**
The following piece of code verifies whether the shape is in a group shape.

{{< gist "aspose-diagram" "92a05cb833bad6d60de2968c96b40ee4" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-VerifyShapeIsInGroup-VerifyShapeIsInGroup.java" >}}

{{% alert color="primary" %}} 

We welcome your queries and suggestions at [Aspose.Diagram Forum](https://forum.aspose.com/c/diagram/17). We'll reply promptly.

{{% /alert %}}
