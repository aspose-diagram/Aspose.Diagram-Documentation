---
title: Spara VSD fil till olika filformat
type: docs
weight: 10
url: /sv/net/save-vsd-file-to-different-file-formats/
---
I den här artikeln jämför vi konverteringsfunktionerna för Aspose.Diagram for .NET med VSTO. Den innehåller .NET kodexempel för att konvertera VSD filer till VDX, PDF och JPEG filformat.
## **VSTO**
VSTO låter dig programmera med Microsoft Visio filer. Så här sparar du en fil i andra format:

1. Skapa ett Visio applikationsobjekt.
1. Gör applikationsobjektet osynligt.
1. Ladda diagram.
1. Spara till VDX, PDF och JPEG.
1. Avsluta applikationsobjektet Visio.

{{< highlight "csharp" >}}

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

{{< /highlight >}}
## **Aspose.Diagram**
Vid programmering med Aspose.Diagram behöver du inte Microsoft Visio på maskinen, och du kan arbeta oberoende av Microsoft Office Automation. Kodavsnitten nedan visar hur man:

1. Ladda ett diagram.
1. Spara diagram till VDX, PDF och JPEG.

{{< highlight "csharp" >}}

 //Load diagram

Diagram vsdDiagram = new Diagram("Drawing.vsd");

//Save the diagram as VDX

vsdDiagram.Save("Drawing1.vdx", SaveFileFormat.VDX);

//Save as PDF

vsdDiagram.Save("Drawing1.pdf", SaveFileFormat.PDF);

//Save as JPEG

vsdDiagram.Save("Drawing1.jpg", SaveFileFormat.JPEG);

{{< /highlight >}}
## **Ladda ner exempelkod**
- [Github](https://github.com/asposemarketplace/Aspose_for_VSTO/releases/download/Aspose.Diagram1.0/Save.VSD.file.to.different.file.formats.VDX.PDF.and.JPEG.Aspose.Diagram.zip)
- [Sourceforge](https://sourceforge.net/projects/asposevsto/files/Aspose.Diagram%20Vs%20VSTO%20Visio/Save%20VSD%20file%20to%20different%20file%20formats%20VDX%20PDF%20and%20JPEG%20\(Aspose.Diagram\).zip/download)
- [Bit hink](https://bitbucket.org/asposemarketplace/aspose-for-vsto/downloads/Save%20VSD%20file%20to%20different%20file%20formats%20VDX%20PDF%20and%20JPEG%20\(Aspose.Diagram\).blixtlås)
