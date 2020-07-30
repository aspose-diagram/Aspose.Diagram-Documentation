---
title : "Aspose.Diagram for Java 17.9 Release Notes" 
description : "" 
weight : 12279 
toc : false
type: docs
url: /java/releasenotes/2017/aspose.diagram+for+java+17.9+release+notes/
---

# Aspose.Diagram for Java : Aspose.Diagram for Java 17.9 Release Notes


This page contains release notes for [Aspose.Diagram for Java 17.9](http://maven.aspose.com/repository/simple/ext-release-local/com/aspose/aspose-diagram/17.9/).

## Improvements and Changes

{{< table style="table-striped" >}}
|Key|Summary|Category|
|:----|:----|:----|
|DIAGRAMJAVA-50485|Add support of auto spacing shapes in Visio|Enhancement|
|DIAGRAMJAVA-50521|Output VSDX - incorrect layout of the connector line |Bug|
|DIAGRAMJAVA-50522|Output PNG - the text of shape goes out of the boundary|Bug|
|DIAGRAMJAVA-50527|Output VSDX - the connecting line is touching the boundary of shape|Bug|
|DIAGRAMJAVA-50540|Output VSDX - incorrect layout of the connecting lines|Bug|
|DIAGRAMJAVA-50543|Output VSDX - incorrect layout and misplaced text of the connecting lines|Bug|
|DIAGRAMJAVA-50545|Output VSDX - Cannot formulate the position of text in shape|Bug|
|DIAGRAMJAVA-50547|Output VSDX - cannot set property value as String|Bug|
{{< /table >}}

## Public API and Backwards Incompatible Changes

See the list for any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.Diagram for Java. If you have concerns about any change listed, please raise it on the [Aspose.Diagram support forum](http://www.aspose.com/community/forums/aspose.diagram-product-family/489/showforum.aspx).

### Adds autoSpaceShapes member in Page

It allows to add auto space among the collection of shapes.

{{< code lang="cs" >}}
AutoSpaceOptions options = new AutoSpaceOptions();
diagram.getPages().getPage(0).autoSpaceShapes(diagram.getPages().getPage(0).getShapes(), options);
{{< /code >}}

### Usage Examples

Please check the list of help topics added in the Aspose.Diagram Wiki docs: 

1.  [Auto-space a Collection of Shapes in the Visio Page](https://docs2.aspose.com/diagram/java/developerguide/workingwithpages/auto-space+a+collection+of+shapes+in+the+visio+page)

