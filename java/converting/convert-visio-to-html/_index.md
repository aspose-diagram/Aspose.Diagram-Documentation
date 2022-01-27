---
title: Convert Visio to HTML format 
linktitle: Convert Visio to HTML
type: docs
weight: 30
url: /java/convert-visio-to-html/
description: This topic show you how to Aspose.Diagram allows to convert Visio to html formats. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to html with a few lines of code.
---

## **Export Visio to HTML**
This article explains how to export a Microsoft Visio diagram to HTML using [Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

Use the [Diagram](http://www.aspose.com/api/java/diagram/aspose.diagram/diagram) class constructor to read the diagram files and the Save method to export the diagram to any supported image format. Developers can save resultant HTML in the local storage or directly to a stream instance.

1. [Save resultant HTML in the local storage](/diagram/java/how-to-convert-a-visio-diagram/).
1. [Save resultant HTML in a stream instance](/diagram/java/how-to-convert-a-visio-diagram/).

The image below shows a VSD file about to be saved to PNG format. You can use other diagram formats (VSDX, VSDM, VSTX, VSSX, VSS, VSSM, VDX, VST, VSTX, VDX, VTX or VSX) as well.

|**Input diagram.**|
| :- |
|![todo:image_alt_text](how-to-convert-a-visio-diagram_6.png)|
In order to export VSD diagram to HTML, perform the following steps:

1. Create an instance of the Diagram class.
1. Call the Dagram class' Save method and set HTML as the output format.
### **Save resultant HTML in the local storage**
The resultant file can be saved by passing a complete path string, including the filename and extension, e.g. @"c:\temp\MyOutput.html".
#### **Save Resultant HTML in Local Storage Programming Sample**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-ExportToHTML-ExportToHTML.cs" >}}



### **Save resultant HTML in a stream instance**
It is for use case to save the resultant HTML in a database or repository without storing it in the local storage. This feature also embeds other resultant resources of the HTML, e.g. fonts, CSS (containing the style information) and images. Since it saves a single HTML file into the stream instance.
#### **Save Resultant HTML in a Stream Programming Sample**
{{< highlight java >}}

 // Load an existing visio diagram

Diagram diagram = new Diagram("Basic Flowchart.vsd");

// Save resultant HTML directly to a stream

MemoryStream stream = new MemoryStream();

diagram.Save(stream, SaveFileFormat.HTML);



{{< /highlight >}}
