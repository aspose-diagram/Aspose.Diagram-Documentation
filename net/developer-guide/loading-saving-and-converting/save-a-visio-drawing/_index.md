---
title: Save a Visio Drawing
type: docs
weight: 20
url: /net/save-a-visio-drawing/
---

## **Visio Drawing Save Overview**
Use the [Diagram.Save]() method to save a Microsoft Visio drawing. There are overloads that allow saving a drawing to file. The drawing can be saved in any save format supported by Aspose.Diagram. For the list of all supported save formats see the [SaveFileFormat]() Enum.
## **Saving Visio Diagram**
The Diagram class of the Aspose.Diagram API represents a Visio drawing and developers can save its Visio diagram object in any supported file format. To save a Microsoft Visio file, simply use the [Diagram.Save]() method, it accepts a file name with a complete path or a file stream object. Aspose.Diagram API infers the save format from the file extension and also offers an additional SaveFileFormat parameter to specify the output file format.
### **Save a Visio Diagram in any Supported File Format**
Using Aspose.Diagram API, developers can save a Visio diagram in any supported file format as listed below:
**VSDX, VSDM, VSSX, VSSM, VSTX, VSTM, VDX, VSX, VTX, TIFF, PNG, BMP, EMF, JPEG, PDF, XPS, GIF, HTML, SVG, SWF and XAML**
### **Saving Diagram Programming Sample**
The example below saves a document to a file.

{{< highlight java >}}

 // Save a Visio diagram

diagram.Save(GetMyDir() + "MyOutput.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
## **Specifying Visio Save Options**
There are several [Diagram.Save]() method overloads that accept a SaveOptions object. This should be an object of a class derived from the SaveOptions class. Each save format has a corresponding class that holds save options for that save format. For example, there is PdfSaveOptions for the SaveFileFormat.PDF save format.
### **Visio Diagram Save Options**
These examples show how to:

- [Use Diagram Save Options](/diagram/net/save-a-visio-drawing-html/).
- [Use PDF Save Options](/diagram/net/save-a-visio-drawing-html/).
- [Use HTML Save Options](/diagram/net/save-a-visio-drawing-html/).
- [Use Image Save Options](/diagram/net/save-a-visio-drawing-html/).
- [Use SVG Save Options](/diagram/net/save-a-visio-drawing-html/).
- [Use SWF Save Options](/diagram/net/save-a-visio-drawing-html/).
#### **Use of the Diagram Save Options**
The code below shows how to set save options before saving a document to Visio format.

{{< gist "aspose-diagram" "cce69e51f567ea17ef24bc35fef0f689" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UseDiagramSaveOptions-UseDiagramSaveOptions.cs" >}}



#### **Use of the PDF Save Options**
The code below shows how to set save options before saving a document to a PDF format.

{{< gist "aspose-diagram" "cce69e51f567ea17ef24bc35fef0f689" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UsePDFSaveOptions-UsePDFSaveOptions.cs" >}}



#### **Use of the HTML Save Options**
The code below shows how to set save options before saving a document to HTML file format.

{{< gist "aspose-diagram" "cce69e51f567ea17ef24bc35fef0f689" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UseHTMLSaveOptions-UseHTMLSaveOptions.cs" >}}



#### **Use of the Image Save Options**
The code below shows how to set save options before saving a document to image file format.



{{< gist "aspose-diagram" "cce69e51f567ea17ef24bc35fef0f689" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UseImageSaveOptions-UseImageSaveOptions.cs" >}}


Use of the SVG Save Options

The code below shows how to set save options before saving a document to SVG format.

{{< gist "aspose-diagram" "cce69e51f567ea17ef24bc35fef0f689" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UseSVGSaveOptions-UseSVGSaveOptions.cs" >}}


Use of the SWF Save Options

The code below shows how to set save options before saving a document to SWF format.

{{< gist "aspose-diagram" "cce69e51f567ea17ef24bc35fef0f689" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UseSWFSaveOptions-UseSWFSaveOptions.cs" >}}

Sometimes, developers need to save or export Visio diagrams to different file formats programmatically (like VDX, PDF, JPEG and so on).
## **Save VSD file to different file formats (VDX, PDF and JPEG)**
This article provides a code example that illustrates how to use [VSTO](/diagram/net/save-a-visio-drawing-html/) and [Aspose.Diagram for .NET](/diagram/net/save-a-visio-drawing-html/) to save a Microsoft Visio VSD file to a VDX file, PDF file or a JPEG file programmatically. Below are parallel code snippets for VSTO and Aspose.Diagram for .NET that explains how to save a VSD file into different file formats. You'll notice that the Aspose.Diagram code is shorter. Feel free to use the code and change it to meet your specific needs.
### **Saving a VSD File to Other Formats with VSTO**
VSTO lets you program with Microsoft Visio files. To save a file to other formats:

1. Create a Visio application object.
1. Make the application object invisible.
1. Load the diagram.
1. Save to VDX, PDF and JPEG.
1. Quit the Visio application object.
#### **Saving a VSD File with VSTO Programming Sample**
{{% alert color="primary" %}} 

using Visio = Microsoft.Office.Interop.Visio;
Imports Visio = Microsoft.Office.Interop.Visio

{{% /alert %}} 

**Example:**

{{< gist "aspose-diagram" "cce69e51f567ea17ef24bc35fef0f689" "Examples-CSharp-Knowledge-Base-SaveDiagramTo-VDX-PDF-JPEG-withVSTO-SaveDiagramTo_VDX_PDF_JPEG_withVSTO.cs" >}}
### ` `**Saving VSD File to Other Formats with Aspose.Diagram for .NET**
Using Aspose.Diagram, developers don't need Microsoft Office Visio in the machine, and they can work independently of Microsoft Office Automation.

The code snippets below show how to:

1. Load a diagram.
1. Save the diagram to VSX, PDF and JPEG.
#### **Saving VSD File with Aspose.Diagram for .NET Programming Sample**
{{% alert color="primary" %}} 

using Aspose.Diagram;
Imports Aspose.Diagram

{{% /alert %}} 

**Example:**

{{< gist "aspose-diagram" "cce69e51f567ea17ef24bc35fef0f689" "Examples-CSharp-Knowledge-Base-SaveDiagramTo-VDX-PDF-JPEG-withAspose-SaveDiagramTo_VDX_PDF_JPEG_withAspose.cs" >}}
