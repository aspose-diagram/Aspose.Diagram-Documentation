---
title: Guarde el archivo VSD en diferentes formatos de archivo
type: docs
weight: 10
url: /es/net/save-vsd-file-to-different-file-formats/
---
In this article, we compare the conversion features of Aspose.Diagram for .NET with VSTO. It contains .NET code samples to convert VSD files to VDX, PDF, and JPEG file formats.
## **VSTO**
VSTO le permite programar con archivos Microsoft Visio. Para guardar un archivo en otros formatos:

1. Cree un objeto de aplicación Visio.
1. Haga que el objeto de la aplicación sea invisible.
1. Cargue el diagram.
1. Save to VDX, PDF, and JPEG.
1. Salga del objeto de aplicación Visio.

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
Al programar con Aspose.Diagram, no necesita Microsoft Visio en la máquina, y puede trabajar independientemente de Microsoft Office Automatización. Los fragmentos de código a continuación muestran cómo:

1. Cargue un diagram.
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
## **Descargar código de muestra**
- [Github](https://github.com/asposemarketplace/Aspose_for_VSTO/releases/download/Aspose.Diagram1.0/Save.VSD.file.to.different.file.formats.VDX.PDF.and.JPEG.Aspose.Diagram.zip)
- [forjafuente](https://sourceforge.net/projects/asposevsto/files/Aspose.Diagram%20Vs%20VSTO%20Visio/Save%20VSD%20file%20to%20different%20file%20formats%20VDX%20PDF%20and%20JPEG%20\(Aspose.Diagram\).zip/descargar)
- [Bitbucket](https://bitbucket.org/asposemarketplace/aspose-for-vsto/downloads/Save%20VSD%20file%20to%20different%20file%20formats%20VDX%20PDF%20and%20JPEG%20\(Aspose.Diagram\).Código Postal)
