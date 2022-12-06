---
title: Speichern Sie die VSD-Datei in verschiedenen Dateiformaten
type: docs
weight: 10
url: /de/net/save-vsd-file-to-different-file-formats/
---
In diesem Artikel vergleichen wir die Konvertierungsfunktionen von Aspose.Diagram for .NET mit VSTO. Es enthält .NET-Codebeispiele zum Konvertieren von VSD-Dateien in die Dateiformate VDX, PDF und JPEG.
## **VSTO**
Mit VSTO können Sie mit Microsoft Visio-Dateien programmieren. So speichern Sie eine Datei in anderen Formaten:

1. Erstellen Sie ein Visio-Anwendungsobjekt.
1. Machen Sie das Anwendungsobjekt unsichtbar.
1. Laden Sie die diagram.
1. Speichern unter VDX, PDF und JPEG.
1. Beenden Sie das Anwendungsobjekt Visio.

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
Beim Programmieren mit Aspose.Diagram benötigen Sie Microsoft Visio nicht an der Maschine und können unabhängig von Microsoft Office Automation arbeiten. Die folgenden Code-Snippets zeigen, wie Sie:

1. Laden Sie eine diagram.
1. Speichern Sie die diagram bis VDX, PDF und JPEG.

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
## **Beispielcode herunterladen**
- [GitHub](https://github.com/asposemarketplace/Aspose_for_VSTO/releases/download/Aspose.Diagram1.0/Save.VSD.file.to.different.file.formats.VDX.PDF.and.JPEG.Aspose.Diagram.zip)
- [Quellenschmiede](https://sourceforge.net/projects/asposevsto/files/Aspose.Diagram%20Vs%20VSTO%20Visio/Save%20VSD%20file%20to%20different%20file%20formats%20VDX%20PDF%20and%20JPEG%20\(Aspose.Diagram\).zip/herunterladen)
- [Bit Bucket](https://bitbucket.org/asposemarketplace/aspose-for-vsto/downloads/Save%20VSD%20file%20to%20different%20file%20formats%20VDX%20PDF%20and%20JPEG%20\(Aspose.Diagram\).Postleitzahl)
