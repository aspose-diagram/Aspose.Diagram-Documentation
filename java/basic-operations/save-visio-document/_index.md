---
title: Save Visio document programmatically
linktitle: Save Visio document
type: docs
weight: 30
url: /java/save-visio-document/
description: This page describes how to save Visio document to file, stream with Aspose.Diagram library.
---

## **Visio Drawing Save Overview**
Use the [Diagram.Save](https://apireference.aspose.com/diagram/java/com.aspose.diagram/diagram#save\(java.lang.String,%20int\)) method to save a Microsoft Visio drawing. There are overloads that allow saving a drawing to file. The drawing can be saved in any save format supported by Aspose.Diagram. For the list of all supported save formats see the [SaveFileFormat](https://apireference.aspose.com/diagram/java/com.aspose.diagram/SaveFileFormat) Enum.
## **Saving Visio Diagram**
The Diagram class of the Aspose.Diagram API represents a Visio drawing and developers can save its Visio diagram object in any supported file format. To save a Microsoft Visio file, simply use the [Diagram.Save](https://apireference.aspose.com/diagram/java/com.aspose.diagram/diagram#save\(java.lang.String,%20int\)) method, it accepts a file name with the complete path or a file stream object. Aspose.Diagram API infers the save format from the file extension and also offers an additional SaveFileFormat parameter to specify output file format.
### **Save a Visio Diagram in any Supported File Format**
Using Aspose.Diagram API, developers can save a Visio diagram in any supported file format as listed below:
**VSDX, VSDM, VSSX, VSSM, VSTX, VSTM, VDX, VSX, VTX, TIFF, PNG, BMP, EMF, JPEG, PDF, XPS, GIF, HTML, SVG and XAML**
### **Saving Diagram Programming Sample**
The example below saves a document to a file.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-SaveVisioDiagram-SaveVisioDiagram.java" >}}
## **Specifying Visio Save Options**
There are several [Diagram.Save](https://apireference.aspose.com/diagram/java/com.aspose.diagram/diagram#save\(java.lang.String,%20int\)) method overloads that accept a SaveOptions object. This should be an object of a class derived from the SaveOptions class. Each save format has a corresponding class that holds save options for that save format, for example, there is PdfSaveOptions for the SaveFileFormat.PDF save format.
### **Visio Diagram Save Options**
These examples show how to:

- [Use Diagram Save Options](/diagram/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
- [Use PDF Save Options](/diagram/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
- [Use HTML Save Options](/diagram/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
- [Use Image Save Options](/diagram/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
- [Use SVG Save Options](/diagram/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
#### **Use of the Diagram Save Options**
The code below shows how to set save options before saving a document to Visio format.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UseDiagramSaveOptions-UseDiagramSaveOptions.java" >}}



#### **Use of the PDF Save Options**
The code below shows how to set save options before saving a document to a PDF format.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UsePDFSaveOptions-UsePDFSaveOptions.java" >}}



#### **Use of the HTML Save Options**
The code below shows how to set save options before saving a document to a HTML format.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UseHTMLSaveOptions-UseHTMLSaveOptions.java" >}}



#### **Use of the Image Save Options**
The code below shows how to set save options before saving a document to a image format.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UseImageSaveOptions-UseImageSaveOptions.java" >}}
#### **Use of the SVG Save Options**
The code below shows how to set save options before saving a document to SVG format.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UseSVGSaveOptions-UseSVGSaveOptions.java" >}}
