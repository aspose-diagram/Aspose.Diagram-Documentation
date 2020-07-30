---
title : "Aspose.Diagram for Java 20.1 Release Notes" 
description : "" 
weight : 12248 
toc : false
type: docs
url: /java/releasenotes/2020/aspose.diagram+for+java+20.1+release+notes/
---

# Aspose.Diagram for Java : Aspose.Diagram for Java 20.1 Release Notes


This page contains release notes information for Aspose.Diagram for Java 20.1.

## Improvements and Changes

{{< table style="table-striped" >}}
|Key|Summary|Category|
|:----|:----|:----|
|DIAGRAMJAVA-50664|Gradient fill not supported in export to SVG|Enhancement|
|DIAGRAMJAVA-50670|Allow loading fonts from memory|Enhancement|
|DIAGRAMJAVA-50681|API is taking long time to load diagram file with large size|Enhancement|
|DIAGRAMJAVA-50381|The network shapes are not being preserved on converting a VSDX to PDF|Bug|
|DIAGRAMJAVA-50386|The images are turned upside down with color difference on converting a VSD to SVG|Bug|
|DIAGRAMJAVA-50679|VSDX to PDF - Connectors are missing in output|Bug|
|DIAGRAMJAVA-50680|Visio to PNG - Output images were cropped out|Bug|
{{< /table >}}

## Public API and Backward Incompatible Changes

The following is a list of any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.Diagram for JAVA. If you have concerns about any change listed, please raise it on the Aspose.Diagram support forum.

*   Added getPages and setPages in Page - Specifies the index of the pages to be loaded.

{{< code lang="cs" >}}
LoadOptions options = new LoadOptions(LoadFileFormat.VSDX);
options.setPages(new ArrayList());
options.getPages().add(0);
{{< /code >}}

*   Adds setFontSources in FontConfigs - Sets the fonts sources.

  

byte\[\] b = new byte\[\] { 0 };com.aspose.diagram.MemoryFontSource sc1 = new com.aspose.diagram.MemoryFontSource(b);com.aspose.diagram.MemoryFontSource sc2 = new com.aspose.diagram.MemoryFontSource(b);com.aspose.diagram.MemoryFontSource\[\] sc = new com.aspose.diagram.MemoryFontSource\[\] { sc1, sc2 };com.aspose.diagram.FontConfigs.setFontSources(sc); 

