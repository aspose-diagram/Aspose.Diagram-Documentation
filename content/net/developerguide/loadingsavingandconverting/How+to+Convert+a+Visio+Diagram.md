+++
title = "How to Convert a Visio Diagram" 
description = "" 
weight = 12017 
+++

Aspose.Diagram for .NET : How to Convert a Visio Diagram  

# Aspose.Diagram for .NET : How to Convert a Visio Diagram


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Export to PDF](#HowtoConvertaVisioDiagram-ExporttoPDF)
    *   1.1 [Export Microsoft Visio Drawing to PDF](#HowtoConvertaVisioDiagram-ExportMicrosoftVisioDrawingtoPDF)
    *   1.2 [Split Multiple Pages](#HowtoConvertaVisioDiagram-SplitMultiplePages)
    *   1.3 [Use Page Save Callback](#HowtoConvertaVisioDiagram-UsePageSaveCallback)
        *   1.3.1 [TestDiagramPageSavingCallback Class](#HowtoConvertaVisioDiagram-TestDiagramPageSavingCallbackClass)
*   2 [Export to XML](#HowtoConvertaVisioDiagram-ExporttoXML)
    *   2.1 [Export Microsoft Visio Drawing to PDF](#HowtoConvertaVisioDiagram-ExportMicrosoftVisioDrawingtoPDF.1)
    *   2.2 [Export VSD to VDX](#HowtoConvertaVisioDiagram-ExportVSDtoVDX)
    *   2.3 [Export from VSD to VSX](#HowtoConvertaVisioDiagram-ExportfromVSDtoVSX)
    *   2.4 [Export VSD to VTX](#HowtoConvertaVisioDiagram-ExportVSDtoVTX)
    *   2.5 [Export Microsoft Visio Drawing to XML](#HowtoConvertaVisioDiagram-ExportMicrosoftVisioDrawingtoXML)
*   3 [Export Diagrams to Image File Formats](#HowtoConvertaVisioDiagram-ExportDiagramstoImageFileFormats)
    *   3.1 [Export Microsoft Visio Drawing to Image File](#HowtoConvertaVisioDiagram-ExportMicrosoftVisioDrawingtoImageFile)
*   4 [Export to XPS](#HowtoConvertaVisioDiagram-ExporttoXPS)
    *   4.1 [Export Microsoft Visio Drawing to XPS](#HowtoConvertaVisioDiagram-ExportMicrosoftVisioDrawingtoXPS)
*   5 [Export Visio to HTML](#HowtoConvertaVisioDiagram-ExportVisiotoHTML)
    *   5.1 [Save resultant HTML in the local storage](#HowtoConvertaVisioDiagram-SaveresultantHTMLinthelocalstorage)
        *   5.1.1 [Save Resultant HTML in Local Storage Programming Sample](#HowtoConvertaVisioDiagram-SaveResultantHTMLinLocalStorageProgrammingSample)
    *   5.2 [Save resultant HTML in a stream instance](#HowtoConvertaVisioDiagram-SaveresultantHTMLinastreaminstance)
        *   5.2.1 [Save Resultant HTML in a Stream Programming Sample](#HowtoConvertaVisioDiagram-SaveResultantHTMLinaStreamProgrammingSample)
*   6 [Export a Diagram to SVG](#HowtoConvertaVisioDiagram-ExportaDiagramtoSVG)
    *   6.1 [Export Microsoft Visio Drawing to SVG](#HowtoConvertaVisioDiagram-ExportMicrosoftVisioDrawingtoSVG)
*   7 [Export to SWF](#HowtoConvertaVisioDiagram-ExporttoSWF)
    *   7.1 [Embedded Viewer Programming Sample](#HowtoConvertaVisioDiagram-EmbeddedViewerProgrammingSample)
    *   7.2 [Without Viewer Programming Sample](#HowtoConvertaVisioDiagram-WithoutViewerProgrammingSample)
*   8 [Export a Diagram to XAML](#HowtoConvertaVisioDiagram-ExportaDiagramtoXAML)
    *   8.1 [Export Microsoft Visio Drawing to XAML](#HowtoConvertaVisioDiagram-ExportMicrosoftVisioDrawingtoXAML)
*   9 [Convert Visio Drawing with Selective Shapes](#HowtoConvertaVisioDiagram-ConvertVisioDrawingwithSelectiveShapes)
    *   9.1 [Convert Visio Drawing with Selective Shapes Programming Sample](#HowtoConvertaVisioDiagram-ConvertVisioDrawingwithSelectiveShapesProgrammingSample)
{{< /panel >}}
 

 

## Export to PDF

Aspose.Diagram for .NET directly writes the information about the API and Version Number in output documents. For example, upon rendering a Drawing to PDF, Aspose.Diagram for .NET populates **Application** field with value 'Aspose.Diagram' and **PDF Producer** field with value, e.g 'Aspose.Diagram 17.9'.

Please note that you cannot instruct Aspose.Diagram for .NET API to change or remove this information from output Documents.

This article explains how to export a Microsoft Visio diagram to PDF using [Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) API.

Use the [Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class constructor to read the diagram files and the `Save` method to export the diagram to any supported image format.

The image below shows the VSD diagram that the code snippets below export PDF. You can use other diagram formats (VSS, VSSM, VDX, VST, VSTX, VDX, VTX or VSX) as well.

{{< table style="table-striped" >}}
|The source file.|
|:----|
|![](https://docs2.aspose.com/diagram/net/attachments/18354608/18547282.png)|
{{< /table >}}

To export VSD diagram to PDF:

1.  Create an instance of the `Diagram` class.
2.  Call the `Diagram` classs `Save` method and set the output format to PDF.

Below is an image of the output PDF file.

{{< table style="table-striped" >}}
|The output PDF file.|
|:----|
|![](https://docs2.aspose.com/diagram/net/attachments/18354608/18547283.png)|
{{< /table >}}

### Export Microsoft Visio Drawing to PDF

The code samples show how to export Microsoft Visio Drawing to PDF using C#.

### Split Multiple Pages

Aspose.Diagram for .NET allows splitting multiple pages while converting the Microsoft Visio Diagram to PDF. The following code snippet shows the functionality.  

### Use Page Save Callback

In case you have multiple pages, Aspose.Diagram for .NET allows using page saving callback while converting the Microsoft Visio Diagram to PDF. The following code snippet shows the functionality.  

#### TestDiagramPageSavingCallback Class

{{< code lang="cs" >}}
public class TestDiagramPageSavingCallback : Aspose.Diagram.Saving.IPageSavingCallback
{
    public void PageStartSaving(Aspose.Diagram.Saving.PageStartSavingArgs args)
    {
        Console.WriteLine("Start saving diagram page {0} of pages {1}", args.PageIndex + 1, args.PageCount);
    }
    public void PageEndSaving(Aspose.Diagram.Saving.PageEndSavingArgs args)
    {
        Console.WriteLine("End saving diagram page {0} of pages {1}", args.PageIndex + 1, args.PageCount);
        //don't output pages after page index 8.
        if (args.PageIndex >= 8)
        {
            args.HasMorePages = false;
        }
    }
}
{{< /code >}}

## Export to XML

### Export Microsoft Visio Drawing to PDF

The code samples show how to export Microsoft Visio Drawing to PDF using C#.

This article explains how to export a Microsoft Visio diagram to XML using [Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) API.

*   VDX defines an XML diagram.
*   VTX defines an XML template.
*   VSX defines an XML stencil.

The [Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class' constructors read a diagram and the `Save` method is used to save, or export, a diagram in a different file format. The code snippets in this article show how to use the `Save` method to save a Visio file to [VDX](https://docs2.aspose.com/diagram/net/developerguide/loadingsavingandconverting/how+to+convert+a+visio+diagram), [VTX](https://docs2.aspose.com/diagram/net/developerguide/loadingsavingandconverting/how+to+convert+a+visio+diagram) and [VSX](https://docs2.aspose.com/diagram/net/developerguide/loadingsavingandconverting/how+to+convert+a+visio+diagram).

The image below shows the diagram that is exported in the code snippets below. The exported file is shown before each code snippet.

{{< table style="table-striped" >}}
|A Microsoft Visio diagram about to be exported.|
|:----|
|![](https://docs2.aspose.com/diagram/net/attachments/18354608/18547188.png)|
{{< /table >}}

### Export VSD to VDX

VDX is a schema-based XML file format that lets you save diagrams in a format that products other than Microsoft Visio can read. It's a useful format for transferring diagrams between software applications and retaining editable data.

To export a VSD diagram to VDX:

1.  Create an instance of the `Diagram` class.
2.  Call the `Diagram` class' `Save` method to write the Visio drawing file to VDX.

{{< table style="table-striped" >}}
|The exported VDX file.|
|:----|
|![](https://docs2.aspose.com/diagram/net/attachments/18354608/18547185.png)|
{{< /table >}}

### Export from VSD to VSX

VSX is an XML format for defining stencils, the basic objects from which a diagram is built up. When a Visio file is converted to VSX, only the stencils are exported.

To export a VSD diagram to VSX:

*   Create an instance of the `Diagram` class.
*   Call the `Diagram` class' `Save` method to write the Visio drawing file to VSX.

### Export VSD to VTX

TVX is an XML representation of a template file and stores the settings for the document.

To export a VSD diagram to VTX:

1.  Create an instance of the `Diagram` class.
2.  Call the `diagram` class' `Save` method to write the Visio drawing file in the VTX format.

### Export Microsoft Visio Drawing to XML

The code samples show how to export Microsoft Visio Drawing to XML using C#.

## Export Diagrams to Image File Formats

This article explains how to export a Microsoft Visio diagram to an image using [Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) API. Use the [Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class constructor to read the diagram files and the `Save` method to export the diagram to any supported image format.

To export a diagram to an image:

*   Create an instance of the `Diagram` class.
*   Call the `Diagram` class' `Save` method and set the image format you want to export to.The output image file looks like the original file.

### Export Microsoft Visio Drawing to Image File

It is also possible to save a particular page to image, instead of the entire document:

## Export to XPS

This article explains how to export a Microsoft Visio diagram to XPS using [Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) API.  
Use the [Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class' constructor to read the diagram files and the `Save` method to export the diagram to any supported image format.

The code snippets in this article takes the diagram below as an input. You can use other diagram formats (VSS, VSSX, VSSM, VDX, VST, VSTX, VDX, VTX or VSX) as well.

{{< table style="table-striped" >}}
|The source document.|
|:----|
|![](https://docs2.aspose.com/diagram/net/attachments/18354608/18547183.png)|
{{< /table >}}

To export VSD diagram to PDF:

1.  Create an instance of the `Diagram` class.
2.  Call the `Diagram` class' `Save` method and set PDF as the output format.

### Export Microsoft Visio Drawing to XPS

The code samples show how to export Microsoft Visio Drawing to XPS using C#.

## Export Visio to HTML

This article explains how to export a Microsoft Visio diagram to HTML using [Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) API.

Use the [Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class constructor to read the diagram files and the `Save` method to export the diagram to any supported image format. Developers can save resultant HTML in the local storage or directly to a stream instance.

1.  [Save resultant HTML in the local storage](https://docs2.aspose.com/diagram/net/developerguide/loadingsavingandconverting/how+to+convert+a+visio+diagram).
2.  [Save resultant HTML in a stream instance](https://docs2.aspose.com/diagram/net/developerguide/loadingsavingandconverting/how+to+convert+a+visio+diagram).

The image below shows a VSD file about to be saved to PNG format. You can use other diagram formats (VSDX, VSDM, VSTX, VSSX, VSS, VSSM, VDX, VST, VSTX, VDX, VTX or VSX) as well.

{{< table style="table-striped" >}}
|Input diagram.|
|:----|
|![](https://docs2.aspose.com/diagram/net/attachments/18354608/18547187.png)|
{{< /table >}}

In order to export VSD diagram to HTML, perform the following steps:

1.  Create an instance of the `Diagram` class.
2.  Call the `Dagram` class' `Save` method and set HTML as the output format.

### Save resultant HTML in the local storage

The resultant file can be saved by passing a complete path string, including the filename and extension, e.g. @"c:\\temp\\MyOutput.html".

#### Save Resultant HTML in Local Storage Programming Sample

  

### Save resultant HTML in a stream instance

It is for use case to save the resultant HTML in a database or repository without storing it in the local storage. This feature also embeds other resultant resources of the HTML, e.g. fonts, CSS (containing the style information) and images. Since it saves a single HTML file into the stream instance.

#### Save Resultant HTML in a Stream Programming Sample

{{< code lang="cs" >}}
// Load an existing visio diagram
Diagram diagram = new Diagram("Basic Flowchart.vsd");

// Save resultant HTML directly to a stream
MemoryStream stream = new MemoryStream();
diagram.Save(stream, SaveFileFormat.HTML);
 
{{< /code >}}

## Export a Diagram to SVG

This article explains how to export a Microsoft Visio diagram to SVG (Scalable Vector Graphics) using [Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) API.

Use the [Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class' constructor to read the diagram files and the `Save` method to export the diagram to any supported image format.

To export VSD diagram to SVG, perform the following steps:

1.  Create an instance of the `Diagram` class.
2.  Call the class' `Save` method and set SVG as the export format.

### Export Microsoft Visio Drawing to SVG

The code samples show how to export a diagram to SVG using C#.

## Export to SWF

This article explains how to export a Microsoft Visio diagram to SWF using [Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) API.

Use the [Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class' constructors to read the diagram files and then the `Diagram` class' `Save` method to export the diagram to SWF format. The image below shows the input VSD file that the code renders to SWF. You can use other diagram formats (VSS, VSSX, VSSM, VDW, VDX, VST, VSTX, VSTM, VDX, VTX or VSX) as well.

{{< table style="table-striped" >}}
|Input diagram.|
|:----|
|![](https://docs2.aspose.com/diagram/net/attachments/18354608/18547186.png)|
{{< /table >}}

  
After the code, there's an image of the output.

To export VSD diagram to SWF::

*   Create an instance of the `Diagram` class.
*   Call the `Diagram` class' `Save` method and provide SWF format to export your diagram to SWF.

### Embedded Viewer Programming Sample

### Without Viewer Programming Sample

The SWF file created by these code snippets include an SWF viewer. Exclude the SWF viewer from the file using the following code.

## Export a Diagram to XAML

This article explains how to export a Microsoft Visio diagram to XAML (Extensible Application Markup Language) using [Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) API.

Use the [Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class' constructor to read the diagram files and the `Save` method to export the diagram to any supported image format.

To export a VSD diagram to XAML:

1.  Create an instance of the `Diagram` class.
2.  Call the class' `Save` method and set XAML as the export format.

### Export Microsoft Visio Drawing to XAML

The code sample show how to export a diagram to XAML using C#.

## Convert Visio Drawing with Selective Shapes

Using Aspose.Diagram API, developers can select a group of shapes to convert a Visio drawing into any other supported format. RenderingSaveOptions class offers a Shapes member to maintain the group of shapes. Each save option class is the extended form of RenderingSaveOptions class.

To export a Visio drawing with selective shapes:

1.  Create an instance of the Diagram class.
2.  Create an instance of any SaveOption class to specify settings as narrated here: [Specify Visio Save Options](http://www.aspose.com/docs/display/diagramnet/Save+a+Visio+Drawing#SaveaVisioDrawing-SpecifyingVisioSaveOptions)
3.  Call Save method of the Diagram class object and pass save option class object as parameter.

### Convert Visio Drawing with Selective Shapes Programming Sample

The code sample shows how to export a drawing with selective Visio shapes.

## Attachments:

![](https://docs2.aspose.com/diagram/net/images/icons/bullet_blue.gif) [Export diagram to PDF-001.png](https://docs2.aspose.com/diagram/net/attachments/18354608/18547282.png) (image/png)  
![](https://docs2.aspose.com/diagram/net/images/icons/bullet_blue.gif) [Export diagram to PDF-002.png](https://docs2.aspose.com/diagram/net/attachments/18354608/18547223.png) (image/png)  
![](https://docs2.aspose.com/diagram/net/images/icons/bullet_blue.gif) [Export diagram to PDF-002.png](https://docs2.aspose.com/diagram/net/attachments/18354608/18547283.png) (image/png)  
![](https://docs2.aspose.com/diagram/net/images/icons/bullet_blue.gif) [Ba9ooeR.png](https://docs2.aspose.com/diagram/net/attachments/18354608/18547184.png) (image/png)  
![](https://docs2.aspose.com/diagram/net/images/icons/bullet_blue.gif) [OJ1jpgh.png](https://docs2.aspose.com/diagram/net/attachments/18354608/18547185.png) (image/png)  
![](https://docs2.aspose.com/diagram/net/images/icons/bullet_blue.gif) [Ba9ooeR.png](https://docs2.aspose.com/diagram/net/attachments/18354608/18547186.png) (image/png)  
![](https://docs2.aspose.com/diagram/net/images/icons/bullet_blue.gif) [P3gaA34.png](https://docs2.aspose.com/diagram/net/attachments/18354608/18547183.png) (image/png)  
![](https://docs2.aspose.com/diagram/net/images/icons/bullet_blue.gif) [WOV36ek.png](https://docs2.aspose.com/diagram/net/attachments/18354608/18547182.png) (image/png)  
![](https://docs2.aspose.com/diagram/net/images/icons/bullet_blue.gif) [XWajazh.png](https://docs2.aspose.com/diagram/net/attachments/18354608/18547188.png) (image/png)  
![](https://docs2.aspose.com/diagram/net/images/icons/bullet_blue.gif) [YX4BNNq.png](https://docs2.aspose.com/diagram/net/attachments/18354608/18547187.png) (image/png)  

