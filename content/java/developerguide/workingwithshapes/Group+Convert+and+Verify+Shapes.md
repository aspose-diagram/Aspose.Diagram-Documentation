+++
title = "Group Convert and Verify Shapes" 
description = "" 
weight = 12035 
+++

Aspose.Diagram for Java : Group, Convert and Verify Shapes  

# Aspose.Diagram for Java : Group, Convert and Verify Shapes


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Group Multiple Shapes Together in the Visio Drawing](#Group,ConvertandVerifyShapes-GroupMultipleShapesTogetherintheVisioDrawing)
    *   1.1 [How to Group Shapes](#Group,ConvertandVerifyShapes-HowtoGroupShapes)
        *   1.1.1 [Group Shapes Programming Sample](#Group,ConvertandVerifyShapes-GroupShapesProgrammingSample)
*   2 [Convert a Visio Shape to Other File Formats](#Group,ConvertandVerifyShapes-ConvertaVisioShapetoOtherFileFormats)
    *   2.1 [Converting a Particular Visio Shape](#Group,ConvertandVerifyShapes-ConvertingaParticularVisioShape)
        *   2.1.1 [Convert Shape Programming Sample](#Group,ConvertandVerifyShapes-ConvertShapeProgrammingSample)
    *   2.2 [Convert Visio Shape to PDF](#Group,ConvertandVerifyShapes-ConvertVisioShapetoPDF)
    *   2.3 [Convert Visio Shape to HTML](#Group,ConvertandVerifyShapes-ConvertVisioShapetoHTML)
*   3 [Verify Whether Two Visio Shapes are Connected or Glued](#Group,ConvertandVerifyShapes-VerifyWhetherTwoVisioShapesareConnectedorGlued)
    *   3.1 [Verification of the Connected or Glued Shapes](#Group,ConvertandVerifyShapes-VerificationoftheConnectedorGluedShapes)
        *   3.1.1 [Verification of Connected or Glued Shapes Programming Sample](#Group,ConvertandVerifyShapes-VerificationofConnectedorGluedShapesProgrammingSample)
*   4 [Verify Whether the Visio Shape is in a Group of Shapes](#Group,ConvertandVerifyShapes-VerifyWhethertheVisioShapeisinaGroupofShapes)
    *   4.1 [Verification of Shape in the Group of Shapes](#Group,ConvertandVerifyShapes-VerificationofShapeintheGroupofShapes)
        *   4.1.1 [Verification of Shape in the Group of Shapes Programming Sample](#Group,ConvertandVerifyShapes-VerificationofShapeintheGroupofShapesProgrammingSample)
{{< /panel >}}
 

 

## Group Multiple Shapes Together in the Visio Drawing

Aspose.Diagram API allows developers in grouping shapes together to move them all at once. Each shape in a group maintains a unique identity and has its own set of properties. When we change the formatting of a group of shapes, it assigns the new property to each shape.

### How to Group Shapes

The `Group` method exposed by the [ShapeCollection](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shapecollection) class can be used to group shapes together.

The code below shows how to:

1.  Load a sample diagram.
2.  initialized an array of the shapes
3.  get a particular shape by id.
4.  get another particular particular shape by id.
5.  assign shapes to the array.
6.  group shapes by calling the `Group` method.
7.  save diagram

#### Group Shapes Programming Sample

Use the following code in your Java application to group shapes together using Aspose.Diagram for Java API.

## Convert a Visio Shape to Other File Formats

Aspose.Diagram for Java API allows developers to convert a single Visio shape to any other supported file format. In this article, we remove all other Visio shapes from the page and customize page setting according to the source Shape size. 

### Converting a Particular Visio Shape

Developers can convert a Visio shape to PDF, HTML, Image, SVG, and SWF by [specifying the Visio save options](#).  
This example code work as follows:

1.  Load a source Visio.
2.  Get a particular page.
3.  Remove the background page.
4.  Build a hash table of all shapes holding the ids and names.
5.  Iterate through the hash table
6.  Remove all shapes from the Visio page, except the particular one.
7.  Set the page size.
8.  Save the Visio page in any supported file format.

#### Convert Shape Programming Sample

### Convert Visio Shape to PDF

The ToPdf method of the Shape class allows to convert a shape into the PDF format.

{{< code lang="cs" >}}
// import diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// save a shape in the PDF format
diagram.getPages().get(0).getShapes().getShape(59).toPdf(dataDir + "out.pdf");
{{< /code >}}

### Convert Visio Shape to HTML

The ToHTML method of the Shape class allows to convert a shape into the HTML format.

{{< code lang="cs" >}}
// import diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
HTMLSaveOptions hs = new HTMLSaveOptions();
// save a shape in the PDF format
diagram.getPages().get(0).getShapes().getShape(59).toHTML(dataDir + "out.pdf", hs);
{{< /code >}}

We welcome your queries and suggestions at [Aspose.Diagram Forum](http://www.aspose.com/community/forums/aspose.diagram-for-java/489/showforum.aspx). We'll reply promptly.

## Verify Whether Two Visio Shapes are Connected or Glued

Aspose.Diagram for Java API allows developers to verify that the two Visio shapes are glued or connected. Previously, we have seen that how we can connect or glue two shapes in these help topics: [Add and Connect Visio Shapes](https://docs2.aspose.com/diagram/java/developerguide/technicalarticles/add+and+connect+visio+shapes) and [Glue Shapes Inside the Container](https://docs2.aspose.com/diagram/java/developerguide/workingwithshapes/working+with+shapes+gluing).

### Verification of the Connected or Glued Shapes

The [Shape](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shape) class offers `IsGlued` and `IsConnected` properties to determine whether two shapes are glued or connected.

#### Verification of Connected or Glued Shapes Programming Sample

The following piece of code verifies whether two shapes are connected or glued.

## Verify Whether the Visio Shape is in a Group of Shapes

Aspose.Diagram for Java API allows developers to verify that the Visio shape is in a group of shapes or not.

### Verification of Shape in the Group of Shapes

The [Shape](https://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shape) class offers `IsInGroup` properties to determine whether the Visio shape is in a group shape.

#### Verification of Shape in the Group of Shapes Programming Sample

The following piece of code verifies whether the shape is in a group shape.

We welcome your queries and suggestions at [Aspose.Diagram Forum](http://www.aspose.com/community/forums/aspose.diagram-for-java/489/showforum.aspx). We'll reply promptly.

