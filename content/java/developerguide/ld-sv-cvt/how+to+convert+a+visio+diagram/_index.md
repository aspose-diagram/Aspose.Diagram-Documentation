---
title : "How to Convert a Visio Diagram" 
description : "" 
weight : 12019 
toc : false
type: docs
url: /java/developerguide/ld-sv-cvt/how+to+convert+a+visio+diagram/
---

# Aspose.Diagram for Java : How to Convert a Visio Diagram


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Exporting to PDF](#exporting-to-pdf)
    *   1.1 [Exporting to PDF Programming Sample](#exporting-to-pdf-programming-sample)
*   2 [Exporting to XML](#exporting-to-xml)
    *   2.1 [Exporting VSD to VDX](#exporting-vsd-to-vdx)
    *   2.2 [Exporting from VSD to VSX](#exporting-from-vsd-to-vsx)
    *   2.3 [Export VSD to VTX](#export-vsd-to-vtx)
    *   2.4 [Exporting to XML Programming Sample](#exporting-to-xml-programming-sample)
*   3 [Exporting Diagrams to Image File Formats](#exporting-diagrams-to-image-file-formats)
    *   3.1 [Exporting to Image File Programming Sample](#exporting-to-image-file-programming-sample)
*   4 [Exporting to XPS](#exporting-to-xps)
    *   4.1 [Exporting to XPS Programming Sample](#exporting-to-xps-programming-sample)
*   5 [Export Visio to HTML](#export-visio-to-html)
    *   5.1 [Save resultant HTML in the local storage](#save-resultant-html-in-the-local-storage)
        *   5.1.1 [Save Resultant HTML in Local Storage Programming Sample](#save-resultant-html-in-local-storage-programming-sample)
    *   5.2 [Save resultant HTML in a stream instance](#save-resultant-html-in-a-stream-instance)
        *   5.2.1 [Save Resultant HTML in a Stream Programming Sample](#save-resultant-html-in-a-stream-programming-sample)
*   6 [Exporting a Diagram to SVG](#exporting-a-diagram-to-svg)
    *   6.1 [Exporting Diagram to SVG Programming Sample](#exporting-diagram-to-svg-programming-sample)
*   7 [Exporting a Diagram to XAML](#exporting-a-diagram-to-xaml)
    *   7.1 [Exporting to XAML Programming Sample](#exporting-to-xaml-programming-sample)
*   8 [Convert Visio Drawing with Selective Shapes](#convert-visio-drawing-with-selective-shapes)
    *   8.1 [Convert Visio Drawing with Selective Shapes Programming Sample](#convert-visio-drawing-with-selective-shapes-programming-sample)
{{< /panel >}}
 

 

## Exporting to PDF

Aspose.Diagram for Java directly writes the information about the API and Version Number in output documents. For example, upon rendering a Drawing to PDF, Aspose.Diagram for Java populates **Application** field with value 'Aspose.Diagram' and **PDF Producer** field with a value, e.g 'Aspose.Diagram 17.9'.

Please note that you cannot instruct Aspose.Diagram for Java API to change or remove this information from output Documents.

This article explains how to export a Microsoft Visio diagram to PDF using [Aspose.Diagram for Java](https://products.aspose.com/diagram/java) API.

Use the [Diagram](https://apireference.aspose.com/java/diagram/com.aspose.diagram/Diagram) class' constructor to read the diagram files and the `Save` method to export the diagram to any supported image format.

The image below shows the VSD diagram that the code snippets below export PDF. You can use other diagram formats (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX or VSX) as well.

**The source file.**

![](https://docs2.aspose.com/diagram/java/attachments/18612238/18809133.png)

To export VSD diagram to PDF:

1.  Create an instance of the `Diagram` class.
2.  Call the `Diagram` classs `Save` method and set the output format to PDF.

Below is an image of the output PDF file.

**The output PDF file.**  
![](https://docs2.aspose.com/diagram/java/attachments/18612238/18809132.png)

### Exporting to PDF Programming Sample

## Exporting to XML

This article explains how to export a Microsoft Visio diagram to XML using [Aspose.Diagram for Java](https://products.aspose.com/diagram/java) API.

*   VDX defines an XML diagram.
*   VTX defines an XML template.
*   VSX defines an XML stencil.

The [Diagram](https://apireference.aspose.com/java/diagram/com.aspose.diagram/Diagram) class' constructors read a diagram and the `Save` method is used to save, or export, a diagram in a different file format. The code snippets in this article show how to use the `Save` method to save a Visio file to [VDX](https://docs2.aspose.com/diagram/java/developerguide/ld-sv-cvt/how+to+convert+a+visio+diagram), [VTX](https://docs2.aspose.com/diagram/java/developerguide/ld-sv-cvt/how+to+convert+a+visio+diagram) and [VSX](https://docs2.aspose.com/diagram/java/developerguide/ld-sv-cvt/how+to+convert+a+visio+diagram).

The image below shows the diagram that is exported in the code snippets below. The exported file is shown before each code snippet.

**A Microsoft Visio diagram about to be exported.**  
![](http://i.imgur.com/XWajazh.png)

### Exporting VSD to VDX

VDX is a schema-based XML file format that lets you save diagrams in a format that products other than Microsoft Visio can read. It's a useful format for transferring diagrams between software applications and retaining editable data.

To export a VSD diagram to VDX:

1.  Create an instance of the `Diagram` class.
2.  Call the `Diagram` class' `Save` method to write the Visio drawing file to VDX.

**The exported VDX file.**  
![](http://i.imgur.com/OJ1jpgh.png)

### Exporting from VSD to VSX

VSX is an XML format for defining stencils, the basic objects from which a diagram is built up. When a Visio file is converted to VSX, only the stencils are exported.

To export a VSD diagram to VSX:

*   Create an instance of the `Diagram` class.
*   Call the `Diagram` class' `Save` method to write the Visio drawing file to VSX.

The image below shows the output VSX file. Note that the stencils used in the diagram, not the diagram itself, are exported.

**The exported VSX file.**  
![](http://i.imgur.com/gkZrxCN.png)

### Export VSD to VTX

TVX is an XML representation of a template file and stores the settings for the document.

To export a VSD diagram to VTX:

1.  Create an instance of the `Diagram` class.
2.  Call the `diagram` class' `Save` method to write the Visio drawing file in the VTX format.

The image below shows the output VTX file.

**The output VTX file.**  
![](http://i.imgur.com/E6pUvGD.jpg)

### Exporting to XML Programming Sample

## Exporting Diagrams to Image File Formats

This article explains how to export a Microsoft Visio diagram to an image using [Aspose.Diagram for Java](https://products.aspose.com/diagram/java) API.

Use the [Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/Diagram) class' constructor to read the diagram files and the `Save` method to export the diagram to any supported image format.The image below shows a VSD file about to be saved to PNG format. You can use other diagram formats (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX or VSX) as well.  
**The source file. Note that the Arrow and Triangle labels are in bold.**  
![](http://i.imgur.com/WOV36ek.png)

To export a diagram to an image:

*   Create an instance of the `Diagram` class.
*   Call the `Diagram` class' `Save` method and set the image format you want to export to.The output image file looks like the original file.

**The output PNG file.**  
![](http://i.imgur.com/WOV36ek.png)

### Exporting to Image File Programming Sample

It is also possible to save a particular page to image, instead of the entire document:

## Exporting to XPS

This article explains how to export a Microsoft Visio diagram to XPS using [Aspose.Diagram for Java](https://products.aspose.com/diagram/java) API.  
Use the [Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/Diagram) class' constructor to read the diagram files and the `Save` method to export the diagram to any supported image format.

The code snippets in this article takes the diagram below as an input. You can use other diagram formats (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX or VSX) as well.

**The source document.**  
![](http://i.imgur.com/P3gaA34.png)

To export VSD diagram to PDF:

1.  Create an instance of the `Diagram` class.
2.  Call the `Diagram` class' `Save` method and set PDF as the output format.

The image below shows the output XPS file.

**The output XPS.**  
![](http://i.imgur.com/1ESRxSy.png)

### Exporting to XPS Programming Sample

## Export Visio to HTML

This article explains how to export a Microsoft Visio diagram to HTML using [Aspose.Diagram for Java](https://products.aspose.com/diagram/java) API.

Use the [Diagram](https://apireference.aspose.com/java/diagram/com.aspose.diagram/Diagram) class constructor to read the diagram files and the `Save` method to export the diagram to any supported image format. Developers can save resultant HTML in the local storage or directly to a stream instance.

1.  [Save resultant HTML in the local storage](https://docs2.aspose.com/diagram/java/developerguide/ld-sv-cvt/how+to+convert+a+visio+diagram).
2.  [Save resultant HTML in a stream instance](https://docs2.aspose.com/diagram/java/developerguide/ld-sv-cvt/how+to+convert+a+visio+diagram).

The image below shows a VSD file about to be saved to PNG format. You can use other diagram formats (VSDX, VSTM, VSTM, VSSX, VSS, VSSM, VDX, VST, VSTX, VDX, VTX or VSX) as well.

**Input diagram.**  
![](http://i.imgur.com/YX4BNNq.png)

In order to export VSD diagram to HTML, perform the following steps:

1.  Create an instance of the `Diagram` class.
2.  Call the `Dagram` class' `Save` method and set HTML as the output format.

The image below shows the output HTML file.

**Output HTML diagram.**  
![](http://i.imgur.com/syavUqI.png)

### Save resultant HTML in the local storage

The resultant file can be saved by passing a complete path string, including the filename and extension, e.g. @"c:\\temp\\MyOutput.html".

#### Save Resultant HTML in Local Storage Programming Sample

  

### Save resultant HTML in a stream instance

It is for use case to save the resultant HTML in a database or repository without storing it in the local storage. This feature also embeds other resultant resources of the HTML, e.g. fonts, CSS (containing the style information) and images. Since it saves a single HTML file into the stream instance.

#### Save Resultant HTML in a Stream Programming Sample

## Exporting a Diagram to SVG

This article explains how to export a Microsoft Visio diagram to SVG (Scalable Vector Graphics) using [Aspose.Diagram for Java](https://products.aspose.com/diagram/java) API.

Use the [Diagram](https://apireference.aspose.com/java/diagram/com.aspose.diagram/Diagram) class' constructor to read the diagram files and the `Save` method to export the diagram to any supported image format.

To export VSD diagram to SVG, perform the following steps:

1.  Create an instance of the `Diagram` class.
2.  Call the class' `Save` method and set SVG as the export format.

### Exporting Diagram to SVG Programming Sample

The code samples show how to export a diagram to SVG using Java.

## Exporting a Diagram to XAML

This article explains how to export a Microsoft Visio diagram to XAML (Extensible Application Markup Language) using [Aspose.Diagram for Java](https://products.aspose.com/diagram/java) API.

Use the [Diagram](https://apireference.aspose.com/java/diagram/com.aspose.diagram/Diagram) class' constructor to read the diagram files and the `Save` method to export the diagram to any supported image format.

To export a VSD diagram to XAML:

1.  Create an instance of the `Diagram` class.
2.  Call the class' `Save` method and set XAML as the export format.

### Exporting to XAML Programming Sample

The code sample show how to export a diagram to XAML using Java.

## Convert Visio Drawing with Selective Shapes

Using Aspose.Diagram API, developers can select a group of shapes to convert a Visio drawing into any other supported format. RenderingSaveOptions class offers a Shapes member to maintain the group of shapes. Each save option class is the extended form of RenderingSaveOptions class.

To export a Visio drawing with selective shapes:

1.  Create an instance of the Diagram class.
2.  Create an instance of any SaveOption class to specify settings as narrated here: [Specify Visio Save Options](http://www.aspose.com/docs/display/diagramjava/Save+a+Visio+Drawing+to+PDF%2C+HTML+and+other+formats#SaveaVisioDrawingtoPDF%2CHTMLandotherformats-SpecifyingVisioSaveOptions)
3.  Call save method of the Diagram class object and pass save option class object as parameter.

### Convert Visio Drawing with Selective Shapes Programming Sample

The code sample shows how to export a drawing with selective Visio shapes.

  

