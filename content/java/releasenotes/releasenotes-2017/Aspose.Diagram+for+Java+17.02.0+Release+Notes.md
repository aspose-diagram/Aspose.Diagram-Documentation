+++
title = "Aspose.Diagram for Java 17.02.0 Release Notes" 
description = "" 
weight = 12286 
+++

Aspose.Diagram for Java : Aspose.Diagram for Java 17.02.0 Release Notes  

# Aspose.Diagram for Java : Aspose.Diagram for Java 17.02.0 Release Notes


This page contains release notes for [Aspose.Diagram for Java 17.02.0](http://maven.aspose.com/repository/simple/ext-release-local/com/aspose/aspose-diagram/17.02.0/).

## Improvements and Changes

{{< table style="table-striped" >}}
|Key|Summary|Category|
|:----|:----|:----|
|DIAGRAMJAVA-50037|VSD to PDF conversion, the background color shade of a group shape is getting changed.|Bug|
|DIAGRAMJAVA-50365|A blank page is generated while converting a Visio page with equations to PNG.|Bug|
|DIAGRAMJAVA-50461|Borders are missing while converting VSDX to PNG.|Bug|
|DIAGRAMJAVA-50462|Symbol disappears while converting VSDX to PNG.|Bug|
|DIAGRAMJAVA-50463|Symbol disappears while converting VSDX to SVG.|Bug|
|DIAGRAMJAVA-50465|Color of the text is different while converting VSDX to PNG.|Bug|
|DIAGRAMJAVA-50466|The text position is incorrect when VSD is converted to SVG format.|Bug|
|DIAGRAMJAVA-50237| \[VSDX to PDF\] - Error message occurred when used LeagueGothic Regular font.|Exception|
{{< /table >}}

## Public API and Backwards Incompatible Changes

See the list for any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.Diagram for Java. If you have concerns about any change listed, please raise it on the [Aspose.Diagram support forum](http://www.aspose.com/community/forums/aspose.diagram-product-family/489/showforum.aspx).

### Adds Shape.getParentShape Method

The `Shape.getParentShape` method allows to get the parent shape of a recent shape.

{{< code lang="cs" >}}
// Call a Diagram class constructor to load the Visio drawing
Diagram diagram = new Diagram("Drawing1.vsdx");
// get a sub-shape by page name, group shape ID, and then sub-shape ID
Shape shape = diagram.getPages().getPage("Page-3").getShapes().getShape(13).getShapes().getShape(2);
Shape parentShape = shape.getParentShape();
System.out.println("Parent Shape's Properties:");
System.out.println("Shape ID: " + parentShape.getID());
System.out.println("Shape Name: " + parentShape.getName());
System.out.println("Shape Type: " + parentShape.getType());
{{< /code >}}

### Adds Shape.isInGroup Method

The `Shape.isInGroup` method allows to detect if the recent shape is part of any group shape.

{{< code lang="cs" >}}
// Call a Diagram class constructor to load the Visio drawing
Diagram diagram = new Diagram("Drawing1.vsdx");
// get a sub-shape by page name, group shape ID, and then sub-shape ID
Shape shape = diagram.getPages().getPage("Page-3").getShapes().getShape(13).getShapes().getShape(2);
System.out.println("Is it in a Group: " + shape.isInGroup());
{{< /code >}}

### Adds Metered Class

The Metered class is added. It allows developers to unlock the evaluation limitations of Aspose.Diagram API as well as track and maintain API licenses. It also monitors the regular usage of Aspose.Diagram API.

{{< code lang="cs" >}}
// Initialize a Metered license class object
Metered metered = new Metered();
// apply public and private keys
metered.setMeteredKey("your-public-key", "your-private-key");
{{< /code >}}

### Usage Examples

Please check the list of help topics added in the Aspose.Diagram Wiki docs:

1.  [Set Public and Private Keys to Apply Metered License](https://docs2.aspose.com/diagram/java/gettingstarted/licensing#licensing-setpublicandprivatekeystoapplymeteredlicense)
2.  [Retrieve the Parent Shape of a Sub-Shape](https://docs.aspose.com/display/diagramjava/Add%2C+Retrieve%2C+Copy+and+Read+Visio+Shape+Data#Add,Retrieve,CopyandReadVisioShapeData-RetrievetheParentShapeofaSub-Shape)
3.  [Verify Whether the Visio Shape is in a Group of Shapes](https://docs2.aspose.com/diagram/java/developerguide/workingwithshapes/group+convert+and+verify+shapes#group,convertandverifyshapes-verifywhetherthevisioshapeisinagroupofshapes)

