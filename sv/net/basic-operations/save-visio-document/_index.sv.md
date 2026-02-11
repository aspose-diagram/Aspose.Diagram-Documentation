---
title: Spara Visio dokument programmatiskt
linktitle: Spara Visio dokument
type: docs
weight: 30
url: /sv/net/save-visio-document/
description: Den här sidan beskriver hur man sparar Visio dokument till fil, streama med Aspose.Diagram bibliotek.
---
## **Visio Ritning Spara Översikt**
 Använd[Diagram.Save]() metod för att spara en Microsoft Visio ritning. Det finns överbelastningar som gör det möjligt att spara en ritning till fil. Ritningen kan sparas i valfritt sparformat som stöds av Aspose.Diagram. För listan över alla sparade format som stöds, se[SaveFileFormat]() Enum.
## **Sparar Visio Diagram**
 Klassen Diagram i Aspose.Diagram API representerar en Visio-ritning och utvecklare kan spara dess Visio diagram-objekt i vilket filformat som helst. För att spara en Microsoft Visio fil, använd helt enkelt[Diagram.Save]()metod, accepterar den ett filnamn med en fullständig sökväg eller ett filströmsobjekt. Aspose.Diagram API härleder sparaformatet från filtillägget och erbjuder även en extra SaveFileFormat-parameter för att specificera utdatafilformatet.
### **Spara ett Visio Diagram i valfritt filformat som stöds**
Genom att använda Aspose.Diagram API kan utvecklare spara en Visio diagram i vilket filformat som helst som stöds enligt listan nedan:
**VSDX, VSDM, VSSX, VSSM, VSTX, VSTM, VDX, VSX, VTX, TIFF, PNG, BMP, EMF, JPEG, PDF, XPS, GIF, HTML, SVG, SWF and XAML**
### **Sparar Diagram Programmeringsexempel**
Exemplet nedan sparar ett dokument till en fil.

{{< highlight "java" >}}

 // Save a Visio diagram

diagram.Save(GetMyDir() + "MyOutput.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
## **Ange Visio Spara alternativ**
 Det finns flera[Diagram.Save]()metodöverbelastningar som accepterar ett SaveOptions-objekt. Detta bör vara ett objekt av en klass som härrör från klassen SaveOptions. Varje sparaformat har en motsvarande klass som innehåller sparaalternativ för det sparade formatet. Det finns till exempel PdfSaveOptions för sparaformatet SaveFileFormat.PDF.
### **Visio Diagram Spara alternativ**
Dessa exempel visar hur man:

- [Använd Diagram Spara alternativ](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Använd PDF Spara alternativ](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Använd HTML Spara alternativ](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Använd alternativ för bildspar](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Använd SVG Spara alternativ](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Använd SWF Spara alternativ](https://docs.aspose.com/diagram/net/save-visio-document/).
#### **Användning av Diagram Spara alternativ**
Koden nedan visar hur du ställer in sparalternativ innan du sparar ett dokument i formatet Visio.

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



#### **Användning av PDF Spara alternativ**
Koden nedan visar hur du ställer in sparalternativ innan du sparar ett dokument i formatet PDF.

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



#### **Användning av HTML Spara alternativ**
Koden nedan visar hur du ställer in sparalternativ innan du sparar ett dokument till filformatet HTML.

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



#### **Användning av bildsparalternativ**
Koden nedan visar hur du ställer in sparalternativ innan du sparar ett dokument i bildfilformat.



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


Användning av SVG Spara alternativ

Koden nedan visar hur du ställer in sparalternativ innan du sparar ett dokument i formatet SVG.

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


Användning av SWF Spara alternativ

Koden nedan visar hur du ställer in sparalternativ innan du sparar ett dokument i formatet SWF.

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

Ibland behöver utvecklare spara eller exportera Visio-diagram till olika filformat programmatiskt (som VDX, PDF, JPEG och så vidare).
## **Spara VSD-filen till olika filformat (VDX, PDF och JPEG)**
 Den här artikeln ger ett kodexempel som illustrerar hur du använder[VSTO](https://docs.aspose.com/diagram/net/save-visio-document/) och[Aspose.Diagram for .NET](https://docs.aspose.com/diagram/net)för att spara en Microsoft Visio VSD fil till en VDX fil, PDF fil eller en JPEG fil programmatiskt. Nedan finns parallella kodavsnitt för VSTO och Aspose.Diagram for .NET som förklarar hur man sparar en VSD-fil i olika filformat. Du kommer att märka att Aspose.Diagram-koden är kortare. Använd gärna koden och ändra den för att möta dina specifika behov.
### **Spara en VSD-fil till andra format med VSTO**
VSTO låter dig programmera med Microsoft Visio filer. Så här sparar du en fil i andra format:

1. Skapa ett Visio applikationsobjekt.
1. Gör applikationsobjektet osynligt.
1. Ladda diagram.
1. Spara till VDX, PDF och JPEG.
1. Avsluta applikationsobjektet Visio.
#### **Spara en VSD-fil med VSTO-programmeringsexempel**
{{% alert color="primary" %}} 

använder Visio = Microsoft.Office.Interop.Visio;
Importer Visio = Microsoft.Office.Interop.Visio

{{% /alert %}} 

**Exempel:**

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
### ` `**Spara VSD-fil till andra format med Aspose.Diagram for .NET**
Med Aspose.Diagram behöver utvecklare inte Microsoft Office Visio i maskinen, och de kan arbeta oberoende av Microsoft Office Automation.

Kodavsnitten nedan visar hur man:

1. Ladda ett diagram.
1. Spara diagram till VSX, PDF och JPEG.
#### **Sparar VSD Fil med Aspose.Diagram for .NET Programmeringsexempel**
{{% alert color="primary" %}} 

använder Aspose.Diagram;
Importer Aspose.Diagram

{{% /alert %}} 

**Exempel:**

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
