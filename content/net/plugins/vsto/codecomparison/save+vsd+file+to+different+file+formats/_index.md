---
title : "Save VSD File to Different File Formats" 
description : "" 
weight : 16095 
toc : false
type: docs
url: /net/plugins/vsto/codecomparison/save+vsd+file+to+different+file+formats/
---

# Aspose.Diagram for .NET : Save VSD File to Different File Formats


{{< panel title="Contents Summary" style="primary" >}}
*   1 [VSTO](#vsto)
*   2 [Aspose.Diagram](#aspose.diagram)
*   3 [Download Sample Code](#download-sample-code)
{{< /panel >}}
 

 

In this article, we compare the conversion features of Aspose.Diagram for .NET with VSTO. It contains .NET code samples to convert VSD files to VDX, PDF, and JPEG file formats.

## VSTO

VSTO lets you program with Microsoft Visio files. To save a file to other formats:

1.  Create a Visio application object.
2.  Make the application object invisible.
3.  Load the diagram.
4.  Save to VDX, PDF, and JPEG.
5.  Quit the Visio application object.

{{< code lang="cs" >}}
//Create Visio Application Object
Visio.Application vsdApp = Application;

//Make Visio Application Invisible
vsdApp.Visible = false;

//Create a document object and load a diagram
Visio.Document vsdDoc = vsdApp.Documents.Open("Drawing.vsd");

//Save the VDX diagram
vsdDoc.SaveAs("Drawing1.vdx");

//Save as PDF file
vsdDoc.ExportAsFixedFormat(Visio.VisFixedFormatTypes.visFixedFormatPDF,
	"Drawing1.pdf", Visio.VisDocExIntent.visDocExIntentScreen,
	Visio.VisPrintOutRange.visPrintAll, 1, vsdDoc.Pages.Count, false, true,
	true, true, true, System.Reflection.Missing.Value);

Visio.Page vsdPage = vsdDoc.Pages[1];

//Save as JPEG Image
vsdPage.Export("Drawing1.jpg");

//Quit Visio Object
vsdApp.Quit();
{{< /code >}}

## Aspose.Diagram

When programming with Aspose.Diagram, you do not need Microsoft Visio on the machine, and you can work independently of Microsoft Office Automation. The code snippets below show how to:

1.  Load a diagram.
2.  Save the diagram to VDX, PDF, and JPEG.

{{< code lang="cs" >}}
//Load diagram
Diagram vsdDiagram = new Diagram("Drawing.vsd");

//Save the diagram as VDX
vsdDiagram.Save("Drawing1.vdx", SaveFileFormat.VDX);

//Save as PDF
vsdDiagram.Save("Drawing1.pdf", SaveFileFormat.PDF);

//Save as JPEG
vsdDiagram.Save("Drawing1.jpg", SaveFileFormat.JPEG);
{{< /code >}}

## Download Sample Code

*   [Codeplex](https://asposevsto.codeplex.com/downloads/get/772933)
*   [Github](https://github.com/asposemarketplace/Aspose_for_VSTO/releases/download/Aspose.Diagram1.0/Save.VSD.file.to.different.file.formats.VDX.PDF.and.JPEG.Aspose.Diagram.zip)
*   [Sourceforge](https://sourceforge.net/projects/asposevsto/files/Aspose.Diagram%20Vs%20VSTO%20Visio/Save%20VSD%20file%20to%20different%20file%20formats%20VDX%20PDF%20and%20JPEG%20(Aspose.Diagram).zip/download)
*   [Bitbucket](https://bitbucket.org/asposemarketplace/aspose-for-vsto/downloads/Save%20VSD%20file%20to%20different%20file%20formats%20VDX%20PDF%20and%20JPEG%20(Aspose.Diagram).zip)

