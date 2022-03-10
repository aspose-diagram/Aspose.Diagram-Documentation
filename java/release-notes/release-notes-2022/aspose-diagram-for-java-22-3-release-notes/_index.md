---
title: Aspose.Diagram for Java 22.3 Release Notes
type: docs
weight: 25
url: /java/aspose-diagram-for-java-22-3-release-notes/
---

{{% alert color="primary" %}}

This page contains release notes information for Aspose.Diagram for Java 22.3.

{{% /alert %}}
## **Improvements and Changes** ##

|**Key**|**Summary**|**Category**|
| :- | :- | :- |
|DIAGRAMJAVA-50883|Determine missing fonts and font substitution information from the API|Bug|

## `?`**Public API and Backward Incompatible Changes**
The following is a list of any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.Diagram for Java. If you have concerns about any change listed, please raise it on the Aspose.Diagram support forum.

### **Adds AddText in Page**
- Adds Text with defined PinX and PinY.

{{< highlight java >}}
Shape shape = page.addText(1, 1, 2, 2, "Test text", "Calibri", "#a5a5a5", 0.25);
{{< /highlight >}}
