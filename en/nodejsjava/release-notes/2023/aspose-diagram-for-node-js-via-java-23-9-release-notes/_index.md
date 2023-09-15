---
title: Aspose.Diagram for Node.js via Java 23.9 Release Notes
type: docs
weight: 19
url: /nodejsjava/aspose-diagram-for-node-js-via-java-23-9-release-notes/
---

{{% alert color="primary" %}}

This page contains release notes information for Aspose.Diagram for Node.js via Java 23.9.

{{% /alert %}}
## **Improvements and Changes** ##

|**Key**|**Summary**|**Category**|
| :- | :- | :- |
|DIAGRAMJAVA-51137|Get shape's inherited group|Enhancement|
|DIAGRAMJAVA-51130|OutOfMemoryError when loading visio|Bug|
|DIAGRAMJAVA-51136|Convert png program exit|Bug|
|DIAGRAMJAVA-51143|Lost shapes in the top|Bug|

## **Public API and Backwards Incompatible Changes**
The following is a list of any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.Diagram for Java. If you have concerns about any change listed, please raise it on the Aspose.Diagram support forum.
### **Adds getInheritGroup in Shape**
- Contains the group for the shape inherit by the master shape.

{{< highlight java >}}
System.out.println("SelectModeValue : " + shape.getInheritGroup().getSelectMode().getValue());
{{< /highlight >}}
