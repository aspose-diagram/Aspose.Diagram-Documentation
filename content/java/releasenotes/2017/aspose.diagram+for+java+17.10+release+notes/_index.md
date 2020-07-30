---
title : "Aspose.Diagram for Java 17.10 Release Notes" 
description : "" 
weight : 12278 
toc : false
type: docs
url: /java/releasenotes/2017/aspose.diagram+for+java+17.10+release+notes/
---

# Aspose.Diagram for Java : Aspose.Diagram for Java 17.10 Release Notes


This page contains release notes for [Aspose.Diagram for Java 17.10](http://maven.aspose.com/repository/simple/ext-release-local/com/aspose/aspose-diagram/17.10/).

## Improvements and Changes

{{< table style="table-striped" >}}
|Key|Summary|Category|
|:----|:----|:----|
|DIAGRAMJAVA-50560|JpegQuality does not make any effect on output document|Enhancement|
|DIAGRAMJAVA-50548|Output VSDX - the connecting line passing through the boundary of the shape|Bug|
|DIAGRAMJAVA-50550|Shape Transform section does not preserve formulas|Bug|
|DIAGRAMJAVA-50551|VSDX to PNG - incorrect rendering of the shape corners|Bug|
|DIAGRAMJAVA-50552|The fill colors are not being preserved on saving a Visio drawing to SVG|Bug|
|DIAGRAMJAVA-50553|Incorrect rendering of lines when saving a Visio drawing to SVG|Bug|
|DIAGRAMJAVA-50554|The fill colors are not being preserved on saving a Visio drawing to SVG|Bug|
|DIAGRAMJAVA-50555|Incorrect rendering of lines when saving a Visio drawing to SVG|Bug|
|DIAGRAMJAVA-50559|VSDM to VDX - the connecting lines are not connected to the shapes|Bug|
|DIAGRAMJAVA-50561|The VSDX drawing is corrupt after adding SolutionXML element|Bug|
{{< /table >}}

### Adds SameAsPdfConversionArea in ImageSaveOptions

It specifies whether to save area in the same way as PDF.

String dataDir = "C:\\\\temp\\\\";// load a drawingDiagram diagram = new Diagram(dataDir + "Drawing1.vsdx");// specify image save optionsImageSaveOptions opts = new ImageSaveOptions(SaveFileFormat.PNG);opts.setSameAsPdfConversionArea(true);

