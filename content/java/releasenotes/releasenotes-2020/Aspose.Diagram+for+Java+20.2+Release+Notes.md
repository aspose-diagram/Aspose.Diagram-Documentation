+++
title = "Aspose.Diagram for Java 20.2 Release Notes" 
description = "" 
weight = 12247 
+++

Aspose.Diagram for Java : Aspose.Diagram for Java 20.2 Release Notes  

# Aspose.Diagram for Java : Aspose.Diagram for Java 20.2 Release Notes


This page contains release notes information for Aspose.Diagram for Java 20.2.

## Improvements and Changes

{{< table style="table-striped" >}}
|Key|Summary|Category|
|:----|:----|:----|
|DIAGRAMJAVA-50361|The shape foreground color is not being preserved on converting a VST to PNG|Enhancement|
|DIAGRAMJAVA-50504|VSD to PDF - the color of lines is changed|Enhancement|
{{< /table >}}

##  Public API and Backward Incompatible Changes

The following is a list of any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.Diagram for Java. If you have concerns about any change listed, please raise it on the Aspose.Diagram support forum.

### Added enlargePage in ImageSaveOptions

*   Specifies whether to enlarge page

{{< code lang="cs" >}}
com.aspose.diagram.ImageSaveOptions o = new com.aspose.diagram.ImageSaveOptions(SaveFileFormat.PNG);
opt.setEnlargePage(false);
{{< /code >}}

### Added hasHiddenInfo in Diagram

*   Indicates whether this diagram has hidden information

diagram.hasHiddenInfo();

