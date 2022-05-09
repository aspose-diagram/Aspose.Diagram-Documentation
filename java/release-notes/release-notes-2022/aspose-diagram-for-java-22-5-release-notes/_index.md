---
title: Aspose.Diagram for Java 22.5 Release Notes
type: docs
weight: 23
url: /java/aspose-diagram-for-java-22-5-release-notes/
---

{{% alert color="primary" %}}

This page contains release notes information for Aspose.Diagram for Java 22.5.

{{% /alert %}}
## **Improvements and Changes** ##

|**Key**|**Summary**|**Category**|
| :- | :- | :- |
|DIAGRAMJAVA-50898|wk: PinPos not defined|Bug|

## `?`**Public API and Backward Incompatible Changes**
The following is a list of any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.Diagram for Java. If you have concerns about any change listed, please raise it on the Aspose.Diagram support forum.

### **Adds getDisplayValue in Field**
- Gets the formatted string value of this field.

{{< highlight java >}}
String str = shape.getFields().get(0).getDisplayValue();
System.out.println(str);
{{< /highlight >}}

### **Adds getInheritParas in Shape**
-  Contains the paras for the shape inherit by the parent style and the master

{{< highlight java >}}
int str = shape.getInheritParas().get(0).getHorzAlign().getValue();
System.out.println(str);
{{< /highlight >}}