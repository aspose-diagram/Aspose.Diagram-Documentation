---
title: Aspose.Diagram for Java 17.12 Release Notes
type: docs
weight: 10
url: /java/aspose-diagram-for-java-17-12-release-notes/
---

{{% alert color="primary" %}} 

This page contains release notes for [Aspose.Diagram for Java 17.12](http://maven.aspose.com/repository/simple/ext-release-local/com/aspose/aspose-diagram/17.12/).

{{% /alert %}} 
## **Improvements and Changes**

|**Key**|**Summary**|**Category**|
| :- | :- | :- |
|DIAGRAMJAVA-50290|Provide the single API to convert a Visio shape to PDF|Enhancement|
|DIAGRAMJAVA-50291|Provide the single API to convert a Visio shape to HTML|Enhancement|
|DIAGRAMJAVA-50572|Shape.connectedShapes method does not retrieve outgoing nodes|Enhancement|
|DIAGRAMJAVA-50391|The flipped images and arrows are generated on converting a VSD to SVG|Bug|
|DIAGRAMJAVA-50570|VSD to PDF - the additional text items are added|Bug|
|DIAGRAMJAVA-50571|Import VSDX - an error occurred in the shape element|Bug|
|DIAGRAMJAVA-50573|VSD to SVG - the lines of a group shape are missing|Bug|
|DIAGRAMJAVA-50575|VSD to SVG - the text items are missing|Bug|
|DIAGRAMJAVA-50576|Import VDX procedure throws a page element error|Bug|
### **Adds Copy member in Shape class**
The copy member takes a target shape instance, as a parameter to clone this shape.

{{< highlight java >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Shape newShape = new Shape();

// copy diagram

newShape.copy(diagram.getPages().get(0).getShapes().get(0));

newShape.setID(3);

newShape.getXForm().getPinX().setValue(1);

newShape.getXForm().getPinY().setValue(1);

{{< /highlight >}}
### **Adds toPdf member in Shape class**
The toPdf member converts a shape into the PDF format.

{{< highlight java >}}

 String dataDir = "C:\\temp\\";

// import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toPdf(dataDir + "out.pdf");

{{< /highlight >}}
### **Adds toHTML member in Shape class**
The toHTML member converts a shape into the PDF format.

{{< highlight java >}}

 String dataDir = "C:\\temp\\";

// import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

HTMLSaveOptions hs = new HTMLSaveOptions();

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toHTML(dataDir + "out.pdf", hs);

{{< /highlight >}}
### **Usage Examples**
Please check the list of help topics added in the Aspose.Diagram Wiki docs:

1. [Copy a Visio Shape to another Shape instance](/diagram/java/working-with-visio-shape-data-html/#workingwithvisioshapedata-copyavisioshapetoanothershapeinstance)
1. [Convert Visio Shape to PDF](/diagram/java/group-2c-convert-and-verify-shapes-html/#group-convertandverifyshapes-convertvisioshapetopdf)
1. [Convert Visio Shape to HTML](/diagram/java/group-2c-convert-and-verify-shapes-html/#group-convertandverifyshapes-convertvisioshapetohtml)


