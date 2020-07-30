---
title : "Aspose.Diagram for Java 18.1 Release Notes" 
description : "" 
weight : 12274 
toc : false
type: docs
url: /java/releasenotes/2018/aspose.diagram+for+java+18.1+release+notes/
---

# Aspose.Diagram for Java : Aspose.Diagram for Java 18.1 Release Notes


This page contains release notes for [Aspose.Diagram for Java 18.1](http://maven.aspose.com/repository/simple/ext-release-local/com/aspose/aspose-diagram/18.1/).

## Improvements and Changes

{{< table style="table-striped" >}}
|Key|Summary|Category|
|:----|:----|:----|
|DIAGRAMJAVA-50200|Add support to duplicate / clone a diagram page|Enhancement|
|DIAGRAMJAVA-50408|An error occurred after removing a page from VSDM|Bug|
|DIAGRAMJAVA-50577|VDX to VSDM - the connecting lines are not properly connected|Bug|
|DIAGRAMJAVA-50578|VDX to VSDM - the connecting lines are not properly connected|Bug|
|DIAGRAMJAVA-50579|Output VDX - placing all Visio shapes on the concurrent point|Bug|
|DIAGRAMJAVA-50580|Output VDX - incorrect layout of the shapes|Bug|
{{< /table >}}

### Adds Copy member in Page class

The copy member takes a target page instance, as a parameter to clone this page.

{{< code lang="cs" >}}
// import diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
Page newPage = new Page(1);
// copy page
newPage.copy(diagram.getPages().get(0));
{{< /code >}}

### Usage Examples

Please check the list of help topics added in the Aspose.Diagram Wiki docs:

1.  [Copy Visio Page to another Page instance](https://docs2.aspose.com/diagram/java/developerguide/workingwithpages/retrieve+get+copy+and+insert+a+page#retrieve,get,copyandinsertapage-copyvisiopagetoanotherpageinstance)

