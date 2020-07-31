---
title : "Save a Visio Drawing" 
description : "" 
weight : 12016 
toc : false
type: docs
url: /net/developerguide/ld-sv-cvt/save+a+visio+drawing/
---

# Aspose.Diagram for .NET : Save a Visio Drawing


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Visio Drawing Save Overview](#visio-drawing-save-overview)
*   2 [Saving Visio Diagram](#saving-visio-diagram)
    *   2.1 [Save a Visio Diagram in any Supported File Format](#save-a-visio-diagram-in-any-supported-file-format)
    *   2.2 [Saving Diagram Programming Sample](#saving-diagram-programming-sample)
*   3 [Specifying Visio Save Options](#specifying-visio-save-options)
    *   3.1 [Visio Diagram Save Options](#visio-diagram-save-options)
        *   3.1.1 [Use of the Diagram Save Options](#use-of-the-diagram-save-options)
        *   3.1.2 [Use of the PDF Save Options](#use-of-the-pdf-save-options)
        *   3.1.3 [Use of the HTML Save Options](#use-of-the-html-save-options)
        *   3.1.4 [Use of the Image Save Options](#use-of-the-image-save-options)
*   4 [Save VSD file to different file formats (VDX, PDF and JPEG)](#save-vsd-file-to-different-file-formats-(vdx,-pdf-and-jpeg)))
    *   4.1 [Saving a VSD File to Other Formats with VSTO](#saving-a-vsd-file-to-other-formats-with-vsto)
        *   4.1.1 [Saving a VSD File with VSTO Programming Sample](#saving-a-vsd-file-with-vsto-programming-sample)
    *   4.2 [Saving VSD File to Other Formats with Aspose.Diagram for .NET](#saving-vsd-file-to-other-formats-with-aspose.diagram-for-.net)
        *   4.2.1 [Saving VSD File with Aspose.Diagram for .NET Programming Sample](#saving-vsd-file-with-aspose.diagram-for-.net-programming-sample)
{{< /panel >}}
 

 

## Visio Drawing Save Overview

Use the [`Diagram.Save`](#) method to save a Microsoft Visio drawing. There are overloads that allow saving a drawing to file. The drawing can be saved in any save format supported by Aspose.Diagram. For the list of all supported save formats see the [`SaveFileFormat`](#) Enum.

## Saving Visio Diagram

The Diagram class of the Aspose.Diagram API represents a Visio drawing and developers can save its Visio diagram object in any supported file format. To save a Microsoft Visio file, simply use the [`Diagram.Save`](#) method, it accepts a file name with a complete path or a file stream object. Aspose.Diagram API infers the save format from the file extension and also offers an additional SaveFileFormat parameter to specify the output file format.

### Save a Visio Diagram in any Supported File Format

Using Aspose.Diagram API, developers can save a Visio diagram in any supported file format as listed below:  
**VSDX, VSDM, VSSX, VSSM, VSTX, VSTM, VDX, VSX, VTX, TIFF, PNG, BMP, EMF, JPEG, PDF, XPS, GIF, HTML, SVG, SWF and XAML**

### Saving Diagram Programming Sample

The example below saves a document to a file.

{{< code lang="cs" >}}
// Save a Visio diagram
diagram.Save(GetMyDir() + "MyOutput.vsdx", SaveFileFormat.VSDX);
{{< /code >}}

## Specifying Visio Save Options

There are several [`Diagram.Save`](#) method overloads that accept a `SaveOptions` object. This should be an object of a class derived from the `SaveOptions` class. Each save format has a corresponding class that holds save options for that save format. For example, there is `PdfSaveOptions` for the `SaveFileFormat.PDF` save format.

### Visio Diagram Save Options

These examples show how to:

*   [Use Diagram Save Options](#use-of-the-diagram-save-options).
*   [Use PDF Save Options](#use-of-the-pdf-save-options).
*   [Use HTML Save Options](#use-of-the-html-save-options).
*   [Use Image Save Options](#use-of-the-image-save-options).
*   [Use SVG Save Options](#use-of-the-svg-save-options).
*   [Use SWF Save Options](#use-of-the-swf-save-options).

#### Use of the Diagram Save Options

The code below shows how to set save options before saving a document to Visio format.

  

#### Use of the PDF Save Options

The code below shows how to set save options before saving a document to a PDF format.

  

#### Use of the HTML Save Options

The code below shows how to set save options before saving a document to HTML file format.

  

#### Use of the Image Save Options

The code below shows how to set save options before saving a document to image file format.

  
#### Use of the SVG Save Options

The code below shows how to set save options before saving a document to SVG format.

  
#### Use of the SWF Save Options

The code below shows how to set save options before saving a document to SWF format.

Sometimes, developers need to save or export Visio diagrams to different file formats programmatically (like VDX, PDF, JPEG and so on).

## Save VSD file to different file formats (VDX, PDF and JPEG)

This article provides a code example that illustrates how to use [VSTO](https://docs2.aspose.com/diagram/net/developerguide/ld-sv-cvt/save+a+visio+drawing) and [Aspose.Diagram for .NET](https://docs2.aspose.com/diagram/net/developerguide/ld-sv-cvt/save+a+visio+drawing) to save a Microsoft Visio VSD file to a VDX file, PDF file or a JPEG file programmatically. Below are parallel code snippets for VSTO and Aspose.Diagram for .NET that explains how to save a VSD file into different file formats. You'll notice that the Aspose.Diagram code is shorter. Feel free to use the code and change it to meet your specific needs.

### Saving a VSD File to Other Formats with VSTO

VSTO lets you program with Microsoft Visio files. To save a file to other formats:

1.  Create a Visio application object.
2.  Make the application object invisible.
3.  Load the diagram.
4.  Save to VDX, PDF and JPEG.
5.  Quit the Visio application object.

#### Saving a VSD File with VSTO Programming Sample

using Visio = Microsoft.Office.Interop.Visio;  
Imports Visio = Microsoft.Office.Interop.Visio

**Example:**

### Saving VSD File to Other Formats with Aspose.Diagram for .NET

Using Aspose.Diagram, developers don't need Microsoft Office Visio in the machine, and they can work independently of Microsoft Office Automation.

The code snippets below show how to:

1.  Load a diagram.
2.  Save the diagram to VSX, PDF and JPEG.

#### Saving VSD File with Aspose.Diagram for .NET Programming Sample

using Aspose.Diagram;  
Imports Aspose.Diagram

**Example:**

