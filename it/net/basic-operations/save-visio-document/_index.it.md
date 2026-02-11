---
title: Salva il documento Visio a livello di codice
linktitle: Salva documento Visio
type: docs
weight: 30
url: /it/net/save-visio-document/
description: Questa pagina descrive come salvare il documento Visio su file, eseguire lo streaming con la libreria Aspose.Diagram.
---
## **Visio Riepilogo salvataggio disegno**
 Utilizzare il[Diagram.Save]() metodo per salvare un disegno Microsoft Visio. Esistono sovraccarichi che consentono di salvare un disegno su file. Il disegno può essere salvato in qualsiasi formato di salvataggio supportato da Aspose.Diagram. Per l'elenco di tutti i formati di salvataggio supportati vedere il[SalvaFileFormat]()Enum.
## **Risparmio Visio Diagram**
 La classe Diagram di Aspose.Diagram API rappresenta un disegno Visio e gli sviluppatori possono salvare il suo oggetto Visio diagram in qualsiasi formato di file supportato. Per salvare un file Microsoft Visio, usa semplicemente il[Diagram.Save]()metodo, accetta un nome file con un percorso completo o un oggetto flusso di file. Aspose.Diagram API deduce il formato di salvataggio dall'estensione del file e offre anche un parametro aggiuntivo SaveFileFormat per specificare il formato del file di output.
### **Salva un Visio Diagram in qualsiasi formato di file supportato**
Utilizzando Aspose.Diagram API, gli sviluppatori possono salvare un Visio diagram in qualsiasi formato di file supportato come elencato di seguito:
**VSDX, VSDM, VSSX, VSSM, VSTX, VSTM, VDX, VSX, VTX, TIFF, PNG, BMP, EMF, JPEG, PDF, XPS, GIF, HTML, SVG, SWF and XAML**
### **Salvataggio Diagram Esempio di programmazione**
L'esempio seguente salva un documento in un file.

{{< highlight "java" >}}

 // Save a Visio diagram

diagram.Save(GetMyDir() + "MyOutput.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
## **Specificando Visio Salva opzioni**
 Ce ne sono diversi[Diagram.Save]() method overloads that accept a SaveOptions object. This should be an object of a class derived from the SaveOptions class. Each save format has a corresponding class that holds save options for that save format. For example, there is PdfSaveOptions for the SaveFileFormat.PDF save format.
### **Visio Diagram Salva opzioni**
Questi esempi mostrano come:

- [Utilizzare Diagram Opzioni di salvataggio](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Utilizzare PDF Opzioni di salvataggio](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Utilizzare HTML Opzioni di salvataggio](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Usa le opzioni di salvataggio delle immagini](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Utilizzare SVG Opzioni di salvataggio](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Utilizzare SWF Opzioni di salvataggio](https://docs.aspose.com/diagram/net/save-visio-document/).
#### **Uso delle opzioni di salvataggio Diagram**
Il codice seguente mostra come impostare le opzioni di salvataggio prima di salvare un documento nel formato Visio.

```
{{< highlight "csharp" >}}
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
```



#### **Uso delle opzioni di salvataggio PDF**
The code below shows how to set save options before saving a document to a PDF format.

```
{{< highlight "csharp" >}}
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
```



#### **Uso delle opzioni di salvataggio HTML**
The code below shows how to set save options before saving a document to HTML file format.

```
{{< highlight "csharp" >}}
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
```



#### **Utilizzo delle opzioni di salvataggio delle immagini**
Il codice seguente mostra come impostare le opzioni di salvataggio prima di salvare un documento in formato file immagine.



```
{{< highlight "csharp" >}}
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
```


Uso delle opzioni di salvataggio SVG

Il codice seguente mostra come impostare le opzioni di salvataggio prima di salvare un documento nel formato SVG.

```
{{< highlight "csharp" >}}
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
```


Uso delle opzioni di salvataggio SWF

Il codice seguente mostra come impostare le opzioni di salvataggio prima di salvare un documento nel formato SWF.

```
{{< highlight "csharp" >}}
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
```

Sometimes, developers need to save or export Visio diagrams to different file formats programmatically (like VDX, PDF, JPEG and so on).
## **Save VSD file to different file formats (VDX, PDF and JPEG)**
 In questo articolo viene fornito un esempio di codice che illustra come utilizzare[VSTO](https://docs.aspose.com/diagram/net/save-visio-document/) e[Aspose.Diagram for .NET](https://docs.aspose.com/diagram/net) to save a Microsoft Visio VSD file to a VDX file, PDF file or a JPEG file programmatically. Below are parallel code snippets for VSTO and Aspose.Diagram for .NET that explains how to save a VSD file into different file formats. You'll notice that the Aspose.Diagram code is shorter. Feel free to use the code and change it to meet your specific needs.
### **Salvataggio di un file VSD in altri formati con VSTO**
VSTO ti consente di programmare con file Microsoft Visio. Per salvare un file in altri formati:

1. Creare un oggetto applicazione Visio.
1. Rendi invisibile l'oggetto dell'applicazione.
1. Carica lo diagram.
1. Save to VDX, PDF and JPEG.
1. Uscire dall'oggetto applicazione Visio.
#### **Salvataggio di un file VSD con un esempio di programmazione VSTO**
{{% alert color="primary" %}} 

utilizzando Visio = Microsoft.Office.Interop.Visio;
Importazioni Visio = Microsoft.Office.Interop.Visio

{{% /alert %}} 

**Esempio:**

```
{{< highlight "csharp" >}}
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
```
### ` `**Salvataggio del file VSD in altri formati con Aspose.Diagram for .NET**
Utilizzando Aspose.Diagram, gli sviluppatori non hanno bisogno di Microsoft Office Visio nella macchina e possono lavorare indipendentemente dall'automazione Microsoft Office.

I frammenti di codice seguenti mostrano come:

1. Carica un diagram.
1. Save the diagram to VSX, PDF and JPEG.
#### **Salvataggio del file VSD con Aspose.Diagram for .NET Esempio di programmazione**
{{% alert color="primary" %}} 

utilizzando il numero Aspose.Diagram;
Importazioni Aspose.Diagram

{{% /alert %}} 

**Esempio:**

```
{{< highlight "csharp" >}}
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
```
