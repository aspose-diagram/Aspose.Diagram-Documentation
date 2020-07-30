---
title : "Aspose.Diagram for Java 18.3 Release Notes" 
description : "" 
weight : 12272 
toc : false
type: docs
url: /java/releasenotes/2018/aspose.diagram+for+java+18.3+release+notes/
---

# Aspose.Diagram for Java : Aspose.Diagram for Java 18.3 Release Notes


This page contains release notes for [Aspose.Diagram for Java 18.3](http://maven.aspose.com/repository/simple/ext-release-local/com/aspose/aspose-diagram/18.3/).

## Improvements and Changes

{{< table style="table-striped" >}}
|Key|Summary|Category|
|:----|:----|:----|
|DIAGRAMJAVA-50592|Add support of the NewValue processing instructions|Enhancement|
|DIAGRAMJAVA-50150|Can't access shape TabsCollection objects|Bug|
|DIAGRAMJAVA-50588|Output VSDX - a large sized shape is added|Bug|
|DIAGRAMJAVA-50593|VSDX to SVG - incorrect text and background colors|Bug|
|DIAGRAMJAVA-50595|Diagram turns to black and white when saving VSDX document|Bug|
{{< /table >}}

### Adds moveTo member in Page class

The moveTo member takes the target page index as a parameter to move the position of page in the Visio drawing.

{{< code lang="cs" >}}
// import diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
Page newPage = new Page(1);
// move page in the diagram
newPage.moveTo(2);
diagram.save(dataDir + "Drawing1.vsdx", SaveFileFormat.VSDX);
{{< /code >}}

### Usage Examples

Please check the list of help topics added in the Aspose.Diagram Wiki docs: 

1.  [Move Page position in the Visio drawing](https://docs2.aspose.com/diagram/java/developerguide/workingwithpages/retrieve+get+copy+and+insert+a+page#retrieve,get,copyandinsertapage-movepagepositioninthevisiodrawing)

