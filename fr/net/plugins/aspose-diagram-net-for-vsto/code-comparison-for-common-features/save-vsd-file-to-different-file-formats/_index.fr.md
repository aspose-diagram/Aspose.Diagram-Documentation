---
title: Enregistrer le fichier VSD dans différents formats de fichier
type: docs
weight: 10
url: /fr/net/save-vsd-file-to-different-file-formats/
---
In this article, we compare the conversion features of Aspose.Diagram for .NET with VSTO. It contains .NET code samples to convert VSD files to VDX, PDF, and JPEG file formats.
## **VSTO**
VSTO vous permet de programmer avec les fichiers Microsoft Visio. Pour enregistrer un fichier dans d'autres formats :

1. Créez un objet d'application Visio.
1. Rendre l'objet d'application invisible.
1. Charger le diagram.
1. Save to VDX, PDF, and JPEG.
1. Quittez l'objet d'application Visio.

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
Lors de la programmation avec Aspose.Diagram, vous n'avez pas besoin de Microsoft Visio sur la machine et vous pouvez travailler indépendamment de Microsoft Office Automation. Les extraits de code ci-dessous montrent comment :

1. Charger un diagram.
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
## **Télécharger l'exemple de code**
- [GithubGenericName](https://github.com/asposemarketplace/Aspose_for_VSTO/releases/download/Aspose.Diagram1.0/Save.VSD.file.to.different.file.formats.VDX.PDF.and.JPEG.Aspose.Diagram.zip)
- [Sourceforge](https://sourceforge.net/projects/asposevsto/files/Aspose.Diagram%20Vs%20VSTO%20Visio/Save%20VSD%20file%20to%20different%20file%20formats%20VDX%20PDF%20and%20JPEG%20\(Aspose.Diagram\).zip/télécharger)
- [Bitbucket](https://bitbucket.org/asposemarketplace/aspose-for-vsto/downloads/Save%20VSD%20file%20to%20different%20file%20formats%20VDX%20PDF%20and%20JPEG%20\(Aspose.Diagram\).Zip *: français)
