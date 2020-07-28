+++
title = "Save a Visio Drawing to PDF HTML and other formats" 
description = "" 
weight = 12020 
+++

Aspose.Diagram for Java : Save a Visio Drawing to PDF, HTML and other formats  

# Aspose.Diagram for Java : Save a Visio Drawing to PDF, HTML and other formats


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Visio Drawing Save Overview](#SaveaVisioDrawingtoPDF,HTMLandotherformats-VisioDrawingSaveOverview)
*   2 [Saving Visio Diagram](#SaveaVisioDrawingtoPDF,HTMLandotherformats-SavingVisioDiagram)
    *   2.1 [Save a Visio Diagram in any Supported File Format](#SaveaVisioDrawingtoPDF,HTMLandotherformats-SaveaVisioDiagraminanySupportedFileFormat)
    *   2.2 [Saving Diagram Programming Sample](#SaveaVisioDrawingtoPDF,HTMLandotherformats-SavingDiagramProgrammingSample)
*   3 [Specifying Visio Save Options](#SaveaVisioDrawingtoPDF,HTMLandotherformats-SpecifyingVisioSaveOptions)
    *   3.1 [Visio Diagram Save Options](#SaveaVisioDrawingtoPDF,HTMLandotherformats-VisioDiagramSaveOptions)
        *   3.1.1 [Use of the Diagram Save Options](#SaveaVisioDrawingtoPDF,HTMLandotherformats-UseoftheDiagramSaveOptions)
        *   3.1.2 [Use of the PDF Save Options](#SaveaVisioDrawingtoPDF,HTMLandotherformats-UseofthePDFSaveOptions)
        *   3.1.3 [Use of the HTML Save Options](#SaveaVisioDrawingtoPDF,HTMLandotherformats-UseoftheHTMLSaveOptions)
        *   3.1.4 [Use of the Image Save Options](#SaveaVisioDrawingtoPDF,HTMLandotherformats-UseoftheImageSaveOptions)
        *   3.1.5 [Use of the SVG Save Options](#SaveaVisioDrawingtoPDF,HTMLandotherformats-UseoftheSVGSaveOptions)
{{< /panel >}}
 

 

## Visio Drawing Save Overview

Use the [`Diagram.Save`](https://apireference.aspose.com/java/diagram/com.aspose.diagram/diagram#save(java.lang.String,%20int)) method to save a Microsoft Visio drawing. There are overloads that allow saving a drawing to file. The drawing can be saved in any save format supported by Aspose.Diagram. For the list of all supported save formats see the [`SaveFileFormat`](https://apireference.aspose.com/java/diagram/com.aspose.diagram/SaveFileFormat) Enum.

## Saving Visio Diagram

The Diagram class of the Aspose.Diagram API represents a Visio drawing and developers can save its Visio diagram object in any supported file format. To save a Microsoft Visio file, simply use the [`Diagram.Save`](https://apireference.aspose.com/java/diagram/com.aspose.diagram/diagram#save(java.lang.String,%20int)) method, it accepts a file name with the complete path or a file stream object. Aspose.Diagram API infers the save format from the file extension and also offers an additional SaveFileFormat parameter to specify output file format.

### Save a Visio Diagram in any Supported File Format

Using Aspose.Diagram API, developers can save a Visio diagram in any supported file format as listed below:  
**VSDX, VSDM, VSSX, VSSM, VSTX, VSTM, VDX, VSX, VTX, TIFF, PNG, BMP, EMF, JPEG, PDF, XPS, GIF, HTML, SVG and XAML**

### Saving Diagram Programming Sample

The example below saves a document to a file.

## Specifying Visio Save Options

There are several [`Diagram.Save`](https://apireference.aspose.com/java/diagram/com.aspose.diagram/diagram#save(java.lang.String,%20int)) method overloads that accept a `SaveOptions` object. This should be an object of a class derived from the `SaveOptions` class. Each save format has a corresponding class that holds save options for that save format, for example, there is `PdfSaveOptions` for the `SaveFileFormat.PDF` save format.

### Visio Diagram Save Options

These examples show how to:

*   [Use Diagram Save Options](https://docs2.aspose.com/diagram/java/developerguide/loadingsavingandconverting/save+a+visio+drawing+to+pdf+html+and+other+formats).
*   [Use PDF Save Options](https://docs2.aspose.com/diagram/java/developerguide/loadingsavingandconverting/save+a+visio+drawing+to+pdf+html+and+other+formats).
*   [Use HTML Save Options](https://docs2.aspose.com/diagram/java/developerguide/loadingsavingandconverting/save+a+visio+drawing+to+pdf+html+and+other+formats).
*   [Use Image Save Options](https://docs2.aspose.com/diagram/java/developerguide/loadingsavingandconverting/save+a+visio+drawing+to+pdf+html+and+other+formats).
*   [Use SVG Save Options](https://docs2.aspose.com/diagram/java/developerguide/loadingsavingandconverting/save+a+visio+drawing+to+pdf+html+and+other+formats).

#### Use of the Diagram Save Options

The code below shows how to set save options before saving a document to Visio format.

  

#### Use of the PDF Save Options

The code below shows how to set save options before saving a document to a PDF format.

  

#### Use of the HTML Save Options

The code below shows how to set save options before saving a document to a HTML format.

  

#### Use of the Image Save Options

The code below shows how to set save options before saving a document to a image format.

#### Use of the SVG Save Options

The code below shows how to set save options before saving a document to SVG format.

