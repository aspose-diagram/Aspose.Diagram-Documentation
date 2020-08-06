---
title: How to Convert a Visio Diagram
type: docs
weight: 30
url: /net/how-to-convert-a-visio-diagram/
---

## **Export to PDF**
{{% alert color="primary" %}} 

Aspose.Diagram for .NET directly writes the information about the API and Version Number in output documents. For example, upon rendering a Drawing to PDF, Aspose.Diagram for .NET populates **Application** field with value 'Aspose.Diagram' and **PDF Producer** field with value, e.g 'Aspose.Diagram 17.9'.

Please note that you cannot instruct Aspose.Diagram for .NET API to change or remove this information from output Documents.

{{% /alert %}} 

This article explains how to export a Microsoft Visio diagram to PDF using [Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) API.

Use the [Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class constructor to read the diagram files and the Save method to export the diagram to any supported image format.

The image below shows the VSD diagram that the code snippets below export PDF. You can use other diagram formats (VSS, VSSM, VDX, VST, VSTX, VDX, VTX or VSX) as well.

|**The source file.**|
| :- |
|![todo:image_alt_text](how-to-convert-a-visio-diagram_1.png)|


To export VSD diagram to PDF:

1. Create an instance of the Diagram class.
1. Call the Diagram classs Save method and set the output format to PDF.

Below is an image of the output PDF file.

|**The output PDF file.**|
| :- |
|![todo:image_alt_text](how-to-convert-a-visio-diagram_2.png)|
### **Export Microsoft Visio Drawing to PDF**
The code samples show how to export Microsoft Visio Drawing to PDF using C#.

{{< gist "aspose-diagram" "cce69e51f567ea17ef24bc35fef0f689" "Examples-CSharp-Load-Save-Convert-ExportToPDF-ExportToPDF.cs" >}}
### **Split Multiple Pages**
Aspose.Diagram for .NET allows splitting multiple pages while converting the Microsoft Visio Diagram to PDF. The following code snippet shows the functionality.  

{{< gist "aspose-com-gists" "9dfca011648b40c82e13a8d894532819" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UsePDFSaveOptions-SplitMultiPages.cs" >}}
### **Use Page Save Callback**
In case you have multiple pages, Aspose.Diagram for .NET allows using page saving callback while converting the Microsoft Visio Diagram to PDF. The following code snippet shows the functionality.  

{{< gist "aspose-com-gists" "9dfca011648b40c82e13a8d894532819" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UsePDFSaveOptions-PageSavingCallback.cs" >}}
#### **TestDiagramPageSavingCallback Class**
{{< highlight java >}}

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

{{< /highlight >}}
## **Export to XML**
### **Export Microsoft Visio Drawing to PDF**
The code samples show how to export Microsoft Visio Drawing to PDF using C#.

{{< gist "aspose-diagram" "cce69e51f567ea17ef24bc35fef0f689" "Examples-CSharp-Load-Save-Convert-ExportToPDF-ExportToPDF.cs" >}}

This article explains how to export a Microsoft Visio diagram to XML using [Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) API.

- VDX defines an XML diagram.
- VTX defines an XML template.
- VSX defines an XML stencil.

The [Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class' constructors read a diagram and the Save method is used to save, or export, a diagram in a different file format. The code snippets in this article show how to use the Save method to save a Visio file to [VDX](/diagram/net/how-to-convert-a-visio-diagram-html/), [VTX](/diagram/net/how-to-convert-a-visio-diagram-html/) and [VSX](/diagram/net/how-to-convert-a-visio-diagram-html/).

The image below shows the diagram that is exported in the code snippets below. The exported file is shown before each code snippet.

|**A Microsoft Visio diagram about to be exported.**|
| :- |
|![todo:image_alt_text](how-to-convert-a-visio-diagram_3.png)|

### **Export VSD to VDX**
VDX is a schema-based XML file format that lets you save diagrams in a format that products other than Microsoft Visio can read. It's a useful format for transferring diagrams between software applications and retaining editable data.

To export a VSD diagram to VDX:

1. Create an instance of the Diagram class.
1. Call the Diagram class' Save method to write the Visio drawing file to VDX.

|**The exported VDX file.**|
| :- |
|![todo:image_alt_text](how-to-convert-a-visio-diagram_4.png)|

### **Export from VSD to VSX**
VSX is an XML format for defining stencils, the basic objects from which a diagram is built up. When a Visio file is converted to VSX, only the stencils are exported.

To export a VSD diagram to VSX:

- Create an instance of the Diagram class.
- Call the Diagram class' Save method to write the Visio drawing file to VSX.
### **Export VSD to VTX**
TVX is an XML representation of a template file and stores the settings for the document.

To export a VSD diagram to VTX:

1. Create an instance of the Diagram class.
1. Call the diagram class' Save method to write the Visio drawing file in the VTX format.
### **Export Microsoft Visio Drawing to XML**
The code samples show how to export Microsoft Visio Drawing to XML using C#.

{{< gist "aspose-diagram" "cce69e51f567ea17ef24bc35fef0f689" "Examples-CSharp-Load-Save-Convert-ExportToXML-ExportToXML.cs" >}}
## **Export Diagrams to Image File Formats**
This article explains how to export a Microsoft Visio diagram to an image using [Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) API. Use the [Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class constructor to read the diagram files and the Save method to export the diagram to any supported image format.

To export a diagram to an image:

- Create an instance of the Diagram class.
- Call the Diagram class' Save method and set the image format you want to export to.The output image file looks like the original file.
### **Export Microsoft Visio Drawing to Image File**
{{< gist "aspose-diagram" "cce69e51f567ea17ef24bc35fef0f689" "Examples-CSharp-Load-Save-Convert-ExportToImage-ExportToImage.cs" >}}

It is also possible to save a particular page to image, instead of the entire document:

{{< gist "aspose-diagram" "cce69e51f567ea17ef24bc35fef0f689" "Examples-CSharp-Load-Save-Convert-ExportPageToImage-ExportPageToImage.cs" >}}
## **Export to XPS**
This article explains how to export a Microsoft Visio diagram to XPS using [Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) API.
Use the [Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class' constructor to read the diagram files and the Save method to export the diagram to any supported image format.

The code snippets in this article takes the diagram below as an input. You can use other diagram formats (VSS, VSSX, VSSM, VDX, VST, VSTX, VDX, VTX or VSX) as well.

|**The source document.**|
| :- |
|![todo:image_alt_text](how-to-convert-a-visio-diagram_5.png)|


To export VSD diagram to PDF:

1. Create an instance of the Diagram class.
1. Call the Diagram class' Save method and set PDF as the output format.
### **Export Microsoft Visio Drawing to XPS**
The code samples show how to export Microsoft Visio Drawing to XPS using C#.

{{< gist "aspose-diagram" "cce69e51f567ea17ef24bc35fef0f689" "Examples-CSharp-Load-Save-Convert-ExportToXPS-ExportToXPS.cs" >}}
## **Export Visio to HTML**
This article explains how to export a Microsoft Visio diagram to HTML using [Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) API.

Use the [Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class constructor to read the diagram files and the Save method to export the diagram to any supported image format. Developers can save resultant HTML in the local storage or directly to a stream instance.

1. [Save resultant HTML in the local storage](/diagram/net/how-to-convert-a-visio-diagram-html/).
1. [Save resultant HTML in a stream instance](/diagram/net/how-to-convert-a-visio-diagram-html/).

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
{{< gist "aspose-diagram" "cce69e51f567ea17ef24bc35fef0f689" "Examples-CSharp-Load-Save-Convert-ExportToHTML-ExportToHTML.cs" >}}



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
## **Export a Diagram to SVG**
This article explains how to export a Microsoft Visio diagram to SVG (Scalable Vector Graphics) using [Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) API.

Use the [Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class' constructor to read the diagram files and the Save method to export the diagram to any supported image format.

To export VSD diagram to SVG, perform the following steps:

1. Create an instance of the Diagram class.
1. Call the class' Save method and set SVG as the export format.
### **Export Microsoft Visio Drawing to SVG**
The code samples show how to export a diagram to SVG using C#.

{{< gist "aspose-diagram" "cce69e51f567ea17ef24bc35fef0f689" "Examples-CSharp-Load-Save-Convert-ExportToSVG-ExportToSVG.cs" >}}
## **Export to SWF**
This article explains how to export a Microsoft Visio diagram to SWF using [Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) API.

Use the [Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class' constructors to read the diagram files and then the Diagram class' Save method to export the diagram to SWF format. The image below shows the input VSD file that the code renders to SWF. You can use other diagram formats (VSS, VSSX, VSSM, VDW, VDX, VST, VSTX, VSTM, VDX, VTX or VSX) as well.

|**Input diagram.**|
| :- |
|![todo:image_alt_text](how-to-convert-a-visio-diagram_7.png)|

After the code, there's an image of the output.

To export VSD diagram to SWF::

- Create an instance of the Diagram class.
- Call the Diagram class' Save method and provide SWF format to export your diagram to SWF.
### **Embedded Viewer Programming Sample**
{{< gist "aspose-diagram" "cce69e51f567ea17ef24bc35fef0f689" "Examples-CSharp-Load-Save-Convert-ExportToSWF-ExportToSWF.cs" >}}
### **Without Viewer Programming Sample**
The SWF file created by these code snippets include an SWF viewer. Exclude the SWF viewer from the file using the following code.

{{< gist "aspose-diagram" "cce69e51f567ea17ef24bc35fef0f689" "Examples-CSharp-Working-Diagrams-ExportToSWFWithoutViewer-ExportToSWFWithoutViewer.cs" >}}
## **Export a Diagram to XAML**
This article explains how to export a Microsoft Visio diagram to XAML (Extensible Application Markup Language) using [Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) API.

Use the [Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class' constructor to read the diagram files and the Save method to export the diagram to any supported image format.

To export a VSD diagram to XAML:

1. Create an instance of the Diagram class.
1. Call the class' Save method and set XAML as the export format.
### **Export Microsoft Visio Drawing to XAML**
The code sample show how to export a diagram to XAML using C#.

{{< gist "aspose-diagram" "cce69e51f567ea17ef24bc35fef0f689" "Examples-CSharp-Load-Save-Convert-ExportToXAML-ExportToXAML.cs" >}}
## **Convert Visio Drawing with Selective Shapes**
Using Aspose.Diagram API, developers can select a group of shapes to convert a Visio drawing into any other supported format. RenderingSaveOptions class offers a Shapes member to maintain the group of shapes. Each save option class is the extended form of RenderingSaveOptions class.

To export a Visio drawing with selective shapes:

1. Create an instance of the Diagram class.
1. Create an instance of any SaveOption class to specify settings as narrated here: [Specify Visio Save Options](http://www.aspose.com/docs/display/diagramnet/Save+a+Visio+Drawing#SaveaVisioDrawing-SpecifyingVisioSaveOptions)
1. Call Save method of the Diagram class object and pass save option class object as parameter.
### **Convert Visio Drawing with Selective Shapes Programming Sample**
The code sample shows how to export a drawing with selective Visio shapes.

{{< gist "aspose-diagram" "cce69e51f567ea17ef24bc35fef0f689" "Examples-CSharp-Load-Save-Convert-ConvertVisioWithSelectiveShapes.cs" >}}
