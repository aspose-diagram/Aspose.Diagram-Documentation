---
title: Salva il file VSD in diversi formati di file
type: docs
weight: 10
url: /it/net/save-vsd-file-to-different-file-formats/
---
In this article, we compare the conversion features of Aspose.Diagram for .NET with VSTO. It contains .NET code samples to convert VSD files to VDX, PDF, and JPEG file formats.
## **VSTO**
VSTO ti consente di programmare con file Microsoft Visio. Per salvare un file in altri formati:

1. Creare un oggetto applicazione Visio.
1. Rendi invisibile l'oggetto dell'applicazione.
1. Carica lo diagram.
1. Save to VDX, PDF, and JPEG.
1. Uscire dall'oggetto applicazione Visio.

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
Quando si programma con Aspose.Diagram, non è necessario Microsoft Visio sulla macchina e si può lavorare indipendentemente dall'automazione Microsoft Office. I frammenti di codice seguenti mostrano come:

1. Carica un diagram.
1. Save the diagram to VDX, PDF, and JPEG.

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
## **Scarica il codice di esempio**
- [Github](https://github.com/asposemarketplace/Aspose_for_VSTO/releases/download/Aspose.Diagram1.0/Save.VSD.file.to.different.file.formats.VDX.PDF.and.JPEG.Aspose.Diagram.zip)
- [SourceForge](https://sourceforge.net/projects/asposevsto/files/Aspose.Diagram%20Vs%20VSTO%20Visio/Save%20VSD%20file%20to%20different%20file%20formats%20VDX%20PDF%20and%20JPEG%20\(Aspose.Diagram\).zip/scarica)
- [Bitbucket](https://bitbucket.org/asposemarketplace/aspose-for-vsto/downloads/Save%20VSD%20file%20to%20different%20file%20formats%20VDX%20PDF%20and%20JPEG%20\(Aspose.Diagram\).cerniera lampo)
