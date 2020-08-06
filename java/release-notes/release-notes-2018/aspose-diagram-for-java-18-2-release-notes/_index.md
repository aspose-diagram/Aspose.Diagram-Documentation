---
title: Aspose.Diagram for Java 18.2 Release Notes
type: docs
weight: 110
url: /java/aspose-diagram-for-java-18-2-release-notes/
---

{{% alert color="primary" %}} 

This page contains release notes for [Aspose.Diagram for Java 18.2](http://maven.aspose.com/repository/simple/ext-release-local/com/aspose/aspose-diagram/18.2/).

{{% /alert %}} 
## **Improvements and Changes**

|**Key**|**Summary**|**Category**|
| :- | :- | :- |
|DIAGRAMJAVA-50587|Add support of retrieving relative Char element of the text part|Enhancement|
|DIAGRAMJAVA-50478|Connector lines are passing through the other shapes on converting a VDX to VSDM|Bug|
|DIAGRAMJAVA-50581|VSDX to PDF - incorrect rendering of the shapes|Bug|
|DIAGRAMJAVA-50582|Output VSDX - the connecting lines are not straight|Bug|
|DIAGRAMJAVA-50583|VSD import - an error occurred in the VisioDocument element|Bug|
|DIAGRAMJAVA-50584|VDX import - an error occurred in the VisioDocument element|Bug|
|DIAGRAMJAVA-50585|VSD import - an error occurred in the VisioDocument element|Bug|
|DIAGRAMJAVA-50586|VSDX to SVG - incorrect border color of the shape|Bug|
### **Adds getInheritChars method in Shape class**
It contains the char values for the shape inherit by the master shape.

{{< highlight java >}}

 CharCollection charCollection = shape.getInheritChars();

{{< /highlight >}}
