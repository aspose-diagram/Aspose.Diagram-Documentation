---
title: Aspose.Diagram for .NET 18.1 Release Notes
type: docs
weight: 120
url: /net/aspose-diagram-for-net-18-1-release-notes/
---

{{% alert color="primary" %}} 

This page contains release notes for [Aspose.Diagram for .NET 18.1](https://www.nuget.org/packages/Aspose.Diagram/18.1.0).

{{% /alert %}} 
## **Improvements and Changes**

|**Key**|**Summary**|**Category**|
| :- | :- | :- |
|DIAGRAMNET-50494|Add support to duplicate / clone a diagram page|Enhancement|
|DIAGRAMNET-51057|The command button is missing after removing a page from VSDM|Enhancement|
|DIAGRAMNET-51422|VSDX to PDF - the shadows are being ignored on process shapes|Enhancement|
|DIAGRAMNET-50467|VSD to PDF conversion, the company corporate logo is misplaced|Bug|
|DIAGRAMNET-50469|VSD to PDF conversion, the radio shape text is slightly up than usual|Bug|
|DIAGRAMNET-51199|Title text is not aligned on saving a VSDM to SVG|Bug|
|DIAGRAMNET-51388|Issues with vsdx files loading and saving|Bug|
|DIAGRAMNET-51398|VSD to PNG - the text position is incorrect|Bug|
|DIAGRAMNET-51407|VSD to JPEG - the text items are misplaced|Bug|
|DIAGRAMNET-51419|Shapes are not resized properly in vsdx file|Bug|
|DIAGRAMNET-51420|VSDX file gets corrupted after loading and saving|Bug|
|DIAGRAMNET-51421|VSDX to PDF - incorrect font color of the text|Bug|
## **Public API and Backwards Incompatible Changes**
The following is a list of any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.Diagram for .NET. If you have concerns about any change listed, please raise them in the [Aspose.Diagram support forum](https://forum.aspose.com/c/diagram).
### **Adds Copy member in Page class**
The Copy member takes a target page instance, as a parameter to clone this page.

{{< highlight java >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page(1);

// copy diagram

newPage.Copy(diagram.Pages[0]);

{{< /highlight >}}
### **Usage Examples**
Please check the list of help topics added in the Aspose.Diagram Wiki docs: 

1. [Copy Visio Page to another Page instance](/diagram/net/retrieve-2c-get-2c-copy-and-insert-a-page-html/#retrieve-get-copyandinsertapage-copyvisiopagetoanotherpageinstance)
