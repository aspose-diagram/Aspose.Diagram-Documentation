---
title: Save a Visio Drawing to PDF, HTML and other formats
type: docs
weight: 30
url: /java/save-a-visio-drawing-to-pdf-html-and-other-formats/
---

## **Visio Drawing Save Overview**
Use the [Diagram.Save](https://apireference.aspose.com/java/diagram/com.aspose.diagram/diagram#save\(java.lang.String,%20int\)) method to save a Microsoft Visio drawing. There are overloads that allow saving a drawing to file. The drawing can be saved in any save format supported by Aspose.Diagram. For the list of all supported save formats see the [SaveFileFormat](https://apireference.aspose.com/java/diagram/com.aspose.diagram/SaveFileFormat) Enum.
## **Saving Visio Diagram**
The Diagram class of the Aspose.Diagram API represents a Visio drawing and developers can save its Visio diagram object in any supported file format. To save a Microsoft Visio file, simply use the [Diagram.Save](https://apireference.aspose.com/java/diagram/com.aspose.diagram/diagram#save\(java.lang.String,%20int\)) method, it accepts a file name with the complete path or a file stream object. Aspose.Diagram API infers the save format from the file extension and also offers an additional SaveFileFormat parameter to specify output file format.
### **Save a Visio Diagram in any Supported File Format**
Using Aspose.Diagram API, developers can save a Visio diagram in any supported file format as listed below:
**VSDX, VSDM, VSSX, VSSM, VSTX, VSTM, VDX, VSX, VTX, TIFF, PNG, BMP, EMF, JPEG, PDF, XPS, GIF, HTML, SVG and XAML**
### **Saving Diagram Programming Sample**
The example below saves a document to a file.

{{< gist "aspose-diagram" "92a05cb833bad6d60de2968c96b40ee4" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-SaveVisioDiagram-SaveVisioDiagram.java" >}}
## **Specifying Visio Save Options**
There are several [Diagram.Save](https://apireference.aspose.com/java/diagram/com.aspose.diagram/diagram#save\(java.lang.String,%20int\)) method overloads that accept a SaveOptions object. This should be an object of a class derived from the SaveOptions class. Each save format has a corresponding class that holds save options for that save format, for example, there is PdfSaveOptions for the SaveFileFormat.PDF save format.
### **Visio Diagram Save Options**
These examples show how to:

- [Use Diagram Save Options](/diagram/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats-html/).
- [Use PDF Save Options](/diagram/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats-html/).
- [Use HTML Save Options](/diagram/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats-html/).
- [Use Image Save Options](/diagram/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats-html/).
- [Use SVG Save Options](/diagram/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats-html/).
#### **Use of the Diagram Save Options**
The code below shows how to set save options before saving a document to Visio format.

{{< gist "aspose-diagram" "92a05cb833bad6d60de2968c96b40ee4" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UseDiagramSaveOptions-UseDiagramSaveOptions.java" >}}



#### **Use of the PDF Save Options**
The code below shows how to set save options before saving a document to a PDF format.

{{< gist "aspose-diagram" "92a05cb833bad6d60de2968c96b40ee4" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UsePDFSaveOptions-UsePDFSaveOptions.java" >}}



#### **Use of the HTML Save Options**
The code below shows how to set save options before saving a document to a HTML format.

{{< gist "aspose-diagram" "92a05cb833bad6d60de2968c96b40ee4" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UseHTMLSaveOptions-UseHTMLSaveOptions.java" >}}



#### **Use of the Image Save Options**
The code below shows how to set save options before saving a document to a image format.

{{< gist "aspose-diagram" "92a05cb833bad6d60de2968c96b40ee4" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UseImageSaveOptions-UseImageSaveOptions.java" >}}
#### **Use of the SVG Save Options**
The code below shows how to set save options before saving a document to SVG format.

{{< gist "aspose-diagram" "92a05cb833bad6d60de2968c96b40ee4" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UseSVGSaveOptions-UseSVGSaveOptions.java" >}}
