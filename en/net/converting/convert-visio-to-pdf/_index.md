---
title: Convert Visio to PDF format 
linktitle: Convert Visio to PDF
type: docs
weight: 10
url: /net/convert-visio-to-pdf/
description: This topic show you how to Aspose.Diagram allows to convert Visio to PDF formats. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to PDF with a few lines of code.
---


## **Export to PDF**
{{% alert color="primary" %}}

Aspose.Diagram for .NET directly writes the information about the API and Version Number in output documents. For example, upon rendering a Drawing to PDF, Aspose.Diagram for .NET populates **Application** field with value 'Aspose.Diagram' and **PDF Producer** field with value, e.g 'Aspose.Diagram 17.9'.

Please note that you cannot instruct Aspose.Diagram for .NET API to change or remove this information from output Documents.

{{% /alert %}}

This article explains how to export a Microsoft Visio diagram to PDF using [Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API.

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

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-ExportToPDF-ExportToPDF.cs" >}}
### **Split Multiple Pages**
Aspose.Diagram for .NET allows splitting multiple pages while converting the Microsoft Visio Diagram to PDF. The following code snippet shows the functionality.  

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UsePDFSaveOptions-SplitMultiPages.cs" >}}
### **Use Page Save Callback**
In case you have multiple pages, Aspose.Diagram for .NET allows using page saving callback while converting the Microsoft Visio Diagram to PDF. The following code snippet shows the functionality.  

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UsePDFSaveOptions-PageSavingCallback.cs" >}}
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
