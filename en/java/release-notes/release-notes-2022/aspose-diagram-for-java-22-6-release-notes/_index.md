---
title: Aspose.Diagram for Java 22.6 Release Notes
type: docs
weight: 22
url: /java/aspose-diagram-for-java-22-6-release-notes/
---

{{% alert color="primary" %}}

This page contains release notes information for Aspose.Diagram for Java 22.6.

{{% /alert %}}
## **Improvements and Changes** ##

|**Key**|**Summary**|**Category**|
| :- | :- | :- |
|DIAGRAMJAVA-50963|WK: Shape distorted after saving to PNG|Enhancement|
|DIAGRAMJAVA-50967|Resizing the lateral line shape [Cont.]|Bug|
|DIAGRAMJAVA-50972|API is not parsing the file correctly|Bug|
|DIAGRAMJAVA-50974|Issue in adding new connection point|Bug|

## **Public API and Backwards Incompatible Changes**
The following is a list of any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.Diagram for Java. If you have concerns about any change listed, please raise it on the Aspose.Diagram support forum.

### **Adds Resolution in HTMLSaveOptions**
- Gets or sets the resolution for the generated html, in dots per inch.

{{< highlight java >}}
HTMLSaveOptions option = new HTMLSaveOptions();
option.setResolution(96);
{{< /highlight >}}