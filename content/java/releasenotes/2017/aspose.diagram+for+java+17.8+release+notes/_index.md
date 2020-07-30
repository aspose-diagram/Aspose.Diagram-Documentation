---
title : "Aspose.Diagram for Java 17.8 Release Notes" 
description : "" 
weight : 12280 
toc : false
type: docs
url: /java/releasenotes/2017/aspose.diagram+for+java+17.8+release+notes/
---

# Aspose.Diagram for Java : Aspose.Diagram for Java 17.8 Release Notes


This page contains release notes for [Aspose.Diagram for Java 17.8](http://maven.aspose.com/repository/simple/ext-release-local/com/aspose/aspose-diagram/17.8/).

## Improvements and Changes

{{< table style="table-striped" >}}
|Key|Summary|Category|
|:----|:----|:----|
|DIAGRAMJAVA-50412|Missing shapes on converting a VST to PNG.|Bug|
|DIAGRAMJAVA-50497|Output VSDX - incorrect layout of all connecting lines.|Bug|
|DIAGRAMJAVA-50500|Output VSDX - the manually added shape size is not being changed.|Bug|
|DIAGRAMJAVA-50511|Output VSDX - misplaced text of the dynamic connector.|Bug|
|DIAGRAMJAVA-50516|Output VSDX - the connecting line passing through another shape.|Bug |
|DIAGRAMJAVA-50517|Output VSDX - the decision shape is becoming larger.|Bug|
|DIAGRAMJAVA-50520|Cannot set the overlapping behavior of connecting lines in a VSDX drawing.|Bug|
|DIAGRAMJAVA-50521|Output VSDX - incorrect layout of the connector line.|Bug|
|DIAGRAMJAVA-50522|Output PNG - the text of shape goes out of the boundary.|Bug|
|DIAGRAMJAVA-50523|Output VSDX - incorrect layout of the connecting line.|Bug|
|DIAGRAMJAVA-50525|Output VSDX - the width formula of any shape is not preserved.|Bug|
|DIAGRAMJAVA-50528|Output VSDX - incorrect size of the shape.|Bug|
|DIAGRAMJAVA-50529|Output VSDX - preserve the Text Transform section formulas.|Bug|
|DIAGRAMJAVA-50531|Output VSDX - the layout of shapes is not according to the width and height in shapesheet.|Bug|
|DIAGRAMJAVA-50533|Output VSDX - incorrect layout of the connecting line.|Bug|
{{< /table >}}

## Public API and Backwards Incompatible Changes

See the list for any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.Diagram for Java. If you have concerns about any change listed, please raise it on the [Aspose.Diagram support forum](http://www.aspose.com/community/forums/aspose.diagram-product-family/489/showforum.aspx).

### Adds Quality member in SVGSaveOptions class 

It gets or sets a value determining the quality of the generated images.

String dataDir = "c:\\\\temp\\\\";// Load an existing drawingDiagram diagram = new Diagram(dataDir + "Drawing1.vsdx");// specify SVG export settingsSVGSaveOptions options = new SVGSaveOptions();// set image qualityoptions.setQuality(100);// save drawing in the SVG formatdiagram.save(dataDir + "UseSVGSaveOptions\_out.svg", options);

### Adds connectShapesViaConnectorIndex method in Page class

It allows to connect shapes using connection indexes.

String dataDir = "c:\\\\temp\\\\";// Load an existing drawingDiagram diagram = new Diagram(dataDir + "Drawing1.vsdx");// get shapes by IDShape shape1 = diagram.getPages().get(0).getShapes().getShape(1);Shape shape2 = diagram.getPages().get(0).getShapes().getShape(2);// add connector shapesShape connector1 = new Shape();long connecter1Id = diagram.addShape(connector1, "Dynamic connector", 0);// connect shapes by index of conneecting pointsdiagram.getPages().get(0).connectShapesViaConnectorIndex(shape1.getID(), 6, shape2.getID(), 3, connecter1Id);// save drawingdiagram.save(dataDir + "UseSVGSaveOptions\_out.vsdx", SaveFileFormat.VSDX);

### Usage Examples

Please check the list of help topics added in the Aspose.Diagram Wiki docs: 

1.  [Use Connection indexes to connect shapes](https://docs2.aspose.com/diagram/java/developerguide/workingwithshapes/working+with+visio+shape+data#workingwithvisioshapedata-useconnectionindexestoconnectshapes)
2.  [Use of the SVG Save Options](https://docs2.aspose.com/diagram/java/developerguide/ld-sv-cvt/save+a+visio+drawing+to+pdf+html+and+other+formats#saveavisiodrawingtopdf,htmlandotherformats-useofthesvgsaveoptions)

