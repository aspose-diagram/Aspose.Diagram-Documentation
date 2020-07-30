---
title : "Aspose.Diagram for Java 19.3 Release Notes" 
description : "" 
weight : 12259 
toc : false
type: docs
url: /java/releasenotes/2019/aspose.diagram+for+java+19.3+release+notes/
---

# Aspose.Diagram for Java : Aspose.Diagram for Java 19.3 Release Notes


This page contains release notes for Aspose.Diagram for Java 19.3

## Improvements and Changes

{{< table style="table-striped" >}}
|Key|Summary|Category|
|:----|:----|:----|
|DIAGRAMJAVA-50339|Add support of retrieving common font directories on operating systems|Enhancement|
|DIAGRAMJAVA-50097|VSD to PDF conversion - Curved lines become a straight line|Bug|
|DIAGRAMJAVA-50161|VTX to HTML conversion - Background picture of the whole diagram is missing|Bug|
|DIAGRAMJAVA-50301|VSD to PDF export - Meta type shapes turn into messy symbols|Bug|
|DIAGRAMJAVA-50464|The shape has rendered incorrectly while converting VSDX to PNG|Bug|
|DIAGRAMJAVA-50652|VISIO to PDF - Output PDF shows error in Adobe Reader|Bug|
{{< /table >}}

## Public API and Backwards Incompatible Changes

The following is a list of any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.Diagram for Java. If you have concerns about any change listed, please raise them in the [Aspose.Diagram support forum](https://forum.aspose.com/c/diagram).

### Adds GetDefaultFontDir in Diagram

Get the Default Fonts folder path

{{< code lang="cs" >}}
 string str =  diagram.getDefaultFontDir();
{{< /code >}}

