---
title: Enregistrer le document Visio par programmation
linktitle: Enregistrer le document Visio
type: docs
weight: 30
url: /fr/net/save-visio-document/
description: Cette page décrit comment enregistrer le document Visio dans un fichier, diffuser avec la bibliothèque Aspose.Diagram.
---
## **Visio Vue d'ensemble de l'enregistrement du dessin**
 Utilisez le[Diagram.Save]() méthode pour enregistrer un dessin Microsoft Visio. Il existe des surcharges qui permettent d'enregistrer un dessin dans un fichier. Le dessin peut être enregistré dans n'importe quel format d'enregistrement pris en charge par Aspose.Diagram. Pour la liste de tous les formats d'enregistrement pris en charge, consultez le[Enregistrer le format de fichier]()Enum.
## **Enregistrement Visio Diagram**
 La classe Diagram du Aspose.Diagram API représente un dessin Visio et les développeurs peuvent enregistrer son objet Visio diagram dans n'importe quel format de fichier pris en charge. Pour enregistrer un fichier Microsoft Visio, utilisez simplement le[Diagram.Save]() il accepte un nom de fichier avec un chemin complet ou un objet de flux de fichier. Aspose.Diagram API déduit le format de sauvegarde de l'extension de fichier et propose également un paramètre supplémentaire SaveFileFormat pour spécifier le format de fichier de sortie.
### **Enregistrez un Visio Diagram dans n'importe quel format de fichier pris en charge**
À l'aide de Aspose.Diagram API, les développeurs peuvent enregistrer un Visio diagram dans n'importe quel format de fichier pris en charge, comme indiqué ci-dessous :
**VSDX, VSDM, VSSX, VSSM, VSTX, VSTM, VDX, VSX, VTX, TIFF, PNG, BMP, EMF, JPEG, PDF, XPS, GIF, HTML, SVG, SWF and XAML**
### **Enregistrement de l'exemple de programmation Diagram**
L'exemple ci-dessous enregistre un document dans un fichier.

{{< highlight "java" >}}

 // Save a Visio diagram

diagram.Save(GetMyDir() + "MyOutput.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
## **Spécification des options d'enregistrement Visio**
 Il y a plusieurs[Diagram.Save]() method overloads that accept a SaveOptions object. This should be an object of a class derived from the SaveOptions class. Each save format has a corresponding class that holds save options for that save format. For example, there is PdfSaveOptions for the SaveFileFormat.PDF save format.
### **Visio Diagram Options de sauvegarde**
Ces exemples montrent comment :

- [Utilisez les options de sauvegarde Diagram](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Utilisez les options de sauvegarde PDF](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Utilisez les options de sauvegarde HTML](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Utiliser les options d'enregistrement d'image](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Utilisez les options de sauvegarde SVG](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Utilisez les options de sauvegarde SWF](https://docs.aspose.com/diagram/net/save-visio-document/).
#### **Utilisation des options de sauvegarde Diagram**
Le code ci-dessous montre comment définir les options d'enregistrement avant d'enregistrer un document au format Visio.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Call the diagram constructor to a VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Options when saving a diagram into Visio format
DiagramSaveOptions options = new DiagramSaveOptions(SaveFileFormat.VSDX);

// Summary:
//     When characters in the diagram are unicode and not be set with correct font
//     value or the font is not installed locally, they may appear as block,
//     image or XPS.  Set the DefaultFont such as MingLiu or MS Gothic to show these
//     characters.
options.DefaultFont = "MS Gothic";

// Summary:
//     Defines whether need enlarge page to fit drawing content or not.
// Remarks:
//     Default value is false.
options.AutoFitPageToDrawingContent = true;

diagram.Save(dataDir + "UseDiagramSaveOptions_out.vsdx", options);

{{< /highlight >}}




#### **Utilisation des options de sauvegarde PDF**
The code below shows how to set save options before saving a document to a PDF format.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Call the diagram constructor to load diagram from a VSDX file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Options when saving a diagram into the PDF format
PdfSaveOptions options = new PdfSaveOptions();

// Discard saving background pages of the Visio diagram
options.SaveForegroundPagesOnly = true;

// Specify the quality of JPEG compression for images (if JPEG compression is used). Default is 95.
options.JpegQuality = 100;

// Specify default font name
options.DefaultFont = "Arial";

// Conformance level for generated PDF document.
options.Compliance = PdfCompliance.Pdf15;

// Load the certificate from disk.
// The other constructor overloads can be used to load certificates from different locations.
X509Certificate2 cert = new X509Certificate2(dataDir + "certificate.pfx", "feyb4lgcfbme");
// Sets a digital signature details. If not set, then no signing will be performed.
options.DigitalSignatureDetails = new PdfDigitalSignatureDetails(cert, "Test Signing", "Aspose Office", DateTime.Now, PdfDigitalSignatureHashAlgorithm.Sha512);

// Set encription details
PdfEncryptionDetails encriptionDetails = new PdfEncryptionDetails("user password", "Owner Password", PdfEncryptionAlgorithm.RC4_128);
options.EncryptionDetails = encriptionDetails;
// Sets the number of pages to render in PDF.
options.PageCount = 2;
// Sets the 0-based index of the first page to render. Default is 0.
options.PageIndex = 0;

// Set page size
PageSize pgSize = new PageSize(PaperSizeFormat.A1);
options.PageSize = pgSize;
// Save in any supported file format
diagram.Save(dataDir + "UsePDFSaveOptions_out.pdf", options);

{{< /highlight >}}




#### **Utilisation des options de sauvegarde HTML**
The code below shows how to set save options before saving a document to HTML file format.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Call the diagram constructor to a VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Options when saving a diagram into the HTML format
HTMLSaveOptions options = new HTMLSaveOptions();

// Summary:
//     value or the font is not installed locally, they may appear as a block,
//     set the DefaultFont such as MingLiu or MS Gothic to show these
//     characters.
options.DefaultFont = "MS Gothic";
// Sets the number of pages to render in HTML.
options.PageCount = 2;
// Sets the 0-based index of the first page to render. Default is 0.
options.PageIndex = 0;

// Set page size
PageSize pgSize = new PageSize(PaperSizeFormat.A1);
options.PageSize = pgSize;
// Discard saving background pages of the Visio diagram
options.SaveForegroundPagesOnly = true;

// Specify whether to save html as a single file, Default value is false.
options.SaveAsSingleFile = true;

// Specify whether to include the toolbar or not. Default value is true.
options.SaveToolBar = false;
// Set title of the HTML document
options.Title = "Title goes here";

// Save in any supported file format
diagram.Save(dataDir + "UseHTMLSaveOptions_out.html", options);

// Save resultant HTML directly to a stream
MemoryStream stream = new MemoryStream();
diagram.Save(stream, SaveFileFormat.HTML);

{{< /highlight >}}




#### **Utilisation des options d'enregistrement d'image**
Le code ci-dessous montre comment définir les options d'enregistrement avant d'enregistrer un document au format de fichier image.




{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Call the diagram constructor to a VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

ImageSaveOptions options = new ImageSaveOptions(SaveFileFormat.JPEG);
// Specify the quality level to use during compositing.
options.CompositingQuality = Aspose.Diagram.Saving.CompositingQuality.HighQuality;

// Sets the brightness for the the generated images.
// This property has effect only when saving to raster image formats.
// The default value is 0.5. The value must be in the range between 0 and 1.
options.ImageBrightness = 1f;

// Summary:
//     value or the font is not installed locally, they may appear as a block,
//     set the DefaultFont such as MingLiu or MS Gothic to show these
//     characters.
options.DefaultFont = "MS Gothic";
// Sets the number of pages to render in image.
options.PageCount = 2;
// Sets the 0-based index of the first page to render. Default is 0.
options.PageIndex = 0;

// Set page size
PageSize pgSize = new PageSize(PaperSizeFormat.A1);
options.PageSize = pgSize;
// Discard saving background pages of the Visio diagram
options.SaveForegroundPagesOnly = true;

// Sets the color mode for the generated images.
options.ImageColorMode = ImageColorMode.BlackAndWhite;

// Sets the contrast for the generated images.
// This property has effect only when saving to raster image formats.
// The default value is 0.5. The value must be in the range between 0 and 1.
options.ImageContrast = 1f;

// Specify the algorithm that is used when images are scaled or rotated.
// This property has effect only when saving to raster image formats.
options.InterpolationMode = Aspose.Diagram.Saving.InterpolationMode.NearestNeighbor;

// The value may vary from 0 to 100 where 0 means worst quality,
// But maximum compression and 100 means best quality but minimum compression.
// The default value is 95.
options.JpegQuality = 100;

// Set a value specifying how pixels are offset during rendering.
options.PixelOffsetMode = Aspose.Diagram.Saving.PixelOffsetMode.HighSpeed;

// Sets the resolution for the generated images, in dots per inch. The default value is 96.
options.Resolution = 2f;

// Sets the zoom factor for the generated images.
// The default value is 1.0. The value must be greater than 0.
options.Scale = 1f;

// Specify whether smoothing (antialiasing) is applied to lines
// And curves and the edges of filled areas.
options.SmoothingMode = Aspose.Diagram.Saving.SmoothingMode.HighQuality;
// Sets the type of compression to apply when saving generated images to the TIFF format.
options.TiffCompression = TiffCompression.Ccitt3;

// Save in any supported file format
diagram.Save(dataDir + "UseImageSaveOptions_out.jpeg", options);

{{< /highlight >}}



Utilisation des options de sauvegarde SVG

Le code ci-dessous montre comment définir les options d'enregistrement avant d'enregistrer un document au format SVG.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

SVGSaveOptions options = new SVGSaveOptions();

// Summary:
//     value or the font is not installed locally, they may appear as a block,
//     set the DefaultFont such as MingLiu or MS Gothic to show these
//     characters.
options.DefaultFont = "MS Gothic";
// Sets the 0-based index of the first page to render. Default is 0.
options.PageIndex = 0;

// Set page size
PageSize pgSize = new PageSize(PaperSizeFormat.A1);
options.PageSize = pgSize;

diagram.Save(dataDir + "UseSVGSaveOptions_out.svg", options);

{{< /highlight >}}



Utilisation des options de sauvegarde SWF

Le code ci-dessous montre comment définir les options d'enregistrement avant d'enregistrer un document au format SWF.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

SWFSaveOptions options = new SWFSaveOptions();

// Summary:
//     value or the font is not installed locally, they may appear as a block,
//     set the DefaultFont such as MingLiu or MS Gothic to show these
//     characters.
options.DefaultFont = "MS Gothic";

// Sets the number of pages to render in SWF.
options.PageCount = 2;

// Sets the 0-based index of the first page to render. Default is 0.
options.PageIndex = 0;
// Discard saving background pages of the Visio diagram
options.SaveForegroundPagesOnly = true;
// Specify whether the generated SWF document should include the integrated document viewer or not.
options.ViewerIncluded = true;

diagram.Save(dataDir + "UseSWFSaveOptions_out.swf", options);

{{< /highlight >}}


Sometimes, developers need to save or export Visio diagrams to different file formats programmatically (like VDX, PDF, JPEG and so on).
## **Save VSD file to different file formats (VDX, PDF and JPEG)**
 Cet article fournit un exemple de code qui illustre comment utiliser[VSTO](https://docs.aspose.com/diagram/net/save-visio-document/) et[Aspose.Diagram for .NET](https://docs.aspose.com/diagram/net) to save a Microsoft Visio VSD file to a VDX file, PDF file or a JPEG file programmatically. Below are parallel code snippets for VSTO and Aspose.Diagram for .NET that explains how to save a VSD file into different file formats. You'll notice that the Aspose.Diagram code is shorter. Feel free to use the code and change it to meet your specific needs.
### **Enregistrement d'un fichier VSD dans d'autres formats avec VSTO**
VSTO vous permet de programmer avec les fichiers Microsoft Visio. Pour enregistrer un fichier dans d'autres formats :

1. Créez un objet d'application Visio.
1. Rendre l'objet d'application invisible.
1. Charger le diagram.
1. Save to VDX, PDF and JPEG.
1. Quittez l'objet d'application Visio.
#### **Enregistrement d'un fichier VSD avec un exemple de programmation VSTO**
{{% alert color="primary" %}} 

en utilisant Visio = Microsoft.Office.Interop.Visio ;
Importations Visio = Microsoft.Office.Interop.Visio

{{% /alert %}} 

**Exemple:**


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_KnowledgeBase();

// Create Visio Application Object
Visio.Application vsdApp = new Visio.Application();

// Make Visio Application Invisible
vsdApp.Visible = false;

// Create a document object and load a diagram
Visio.Document vsdDoc = vsdApp.Documents.Open(dataDir + "Drawing1.vsd");

// Save the VDX diagram
vsdDoc.SaveAs(dataDir + "SaveDiagramToVDXwithVSTO_out.vdx");

// Save as PDF file
vsdDoc.ExportAsFixedFormat(Visio.VisFixedFormatTypes.visFixedFormatPDF,
    dataDir + "SaveDiagramToPDFwithVSTO_out.pdf", Visio.VisDocExIntent.visDocExIntentScreen,
    Visio.VisPrintOutRange.visPrintAll, 1, vsdDoc.Pages.Count, false, true,
    true, true, true, System.Reflection.Missing.Value);

Visio.Page vsdPage = vsdDoc.Pages[1];

// Save as JPEG Image
vsdPage.Export(dataDir + "SaveDiagramToJPGwithVSTO_out.jpg");

// Quit Visio Object
vsdApp.Quit();

{{< /highlight >}}

### ` `**Enregistrement du fichier VSD dans d'autres formats avec Aspose.Diagram for .NET**
En utilisant Aspose.Diagram, les développeurs n'ont pas besoin de Microsoft Office Visio dans la machine, et ils peuvent travailler indépendamment de Microsoft Office Automation.

Les extraits de code ci-dessous montrent comment :

1. Charger un diagram.
1. Save the diagram to VSX, PDF and JPEG.
#### **Enregistrement du fichier VSD avec l'exemple de programmation Aspose.Diagram for .NET**
{{% alert color="primary" %}} 

en utilisant Aspose.Diagram ;
Importations Aspose.Diagram

{{% /alert %}} 

**Exemple:**


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_KnowledgeBase();

// Load an exiting Visio diagram
Diagram vsdDiagram = new Diagram(dataDir + "Drawing1.vsd");

// Save the diagram as VDX
vsdDiagram.Save(dataDir + "SaveDiagramToVDXwithAspose_out.vdx", SaveFileFormat.VDX);

// Save as PDF
vsdDiagram.Save(dataDir + "SaveDiagramToPDFwithAspose_out.pdf", SaveFileFormat.PDF);

// Save as JPEG
vsdDiagram.Save(dataDir + "SaveDiagramToJPGwithAspose_out.jpg", SaveFileFormat.JPEG);

{{< /highlight >}}

