---
title: Enregistrer le document Visio par programmation
linktitle: Enregistrer le document Visio
type: docs
weight: 30
url: /fr/java/save-visio-document/
description: Cette page décrit comment enregistrer le document Visio dans un fichier, diffuser avec la bibliothèque Aspose.Diagram.
---
## **Visio Vue d'ensemble de l'enregistrement du dessin**
 Utilisez le[Diagram.Save](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram#save\(java.lang.String,%20int\) pour enregistrer un dessin Microsoft Visio. Il existe des surcharges qui permettent d'enregistrer un dessin dans un fichier. Le dessin peut être enregistré dans n'importe quel format d'enregistrement pris en charge par Aspose.Diagram. Pour la liste de tous les formats d'enregistrement pris en charge, consultez le[Enregistrer le format de fichier](https://reference.aspose.com/diagram/java/com.aspose.diagram/SaveFileFormat)Enum.
## **Enregistrement Visio Diagram**
 La classe Diagram du Aspose.Diagram API représente un dessin Visio et les développeurs peuvent enregistrer son objet Visio diagram dans n'importe quel format de fichier pris en charge. Pour enregistrer un fichier Microsoft Visio, utilisez simplement le[Diagram.Save](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram#save\(java.lang.String,%20int\)), il accepte un nom de fichier avec le chemin complet ou un objet de flux de fichier. Aspose.Diagram API déduit le format de sauvegarde de l'extension de fichier et offre également un paramètre supplémentaire SaveFileFormat pour spécifier le format du fichier de sortie.
### **Enregistrez un Visio Diagram dans n'importe quel format de fichier pris en charge**
À l'aide de Aspose.Diagram API, les développeurs peuvent enregistrer un Visio diagram dans n'importe quel format de fichier pris en charge, comme indiqué ci-dessous :
**VSDX, VSDM, VSSX, VSSM, VSTX, VSTM, VDX, VSX, VTX, TIFF, PNG, BMP, EMF, JPEG, PDF, XPS, GIF, HTML, SVG and XAML**
### **Enregistrement de l'exemple de programmation Diagram**
L'exemple ci-dessous enregistre un document dans un fichier.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SaveVisioDiagram.class);
// load an existing Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// save diagram using the direct path
diagram.save(dataDir + "SaveVisioDiagram_Out.vsdx", SaveFileFormat.VSDX);

		ByteArrayOutputStream dstStream = new ByteArrayOutputStream();
// save diagram in the stream
		diagram.save(dstStream, SaveFileFormat.VSDX);
		// In you want to read the result into a Diagram object again, in Java you need to get the
		// data bytes and wrap into an input stream.
		ByteArrayInputStream srcStream = new ByteArrayInputStream(dstStream.toByteArray());

{{< /highlight >}}
```
## **Spécification des options d'enregistrement Visio**
 Il y a plusieurs[Diagram.Save](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram#save\(java.lang.String,%20int\)) method overloads that accept a SaveOptions object. This should be an object of a class derived from the SaveOptions class. Each save format has a corresponding class that holds save options for that save format, for example, there is PdfSaveOptions for the SaveFileFormat.PDF save format.
### **Visio Diagram Options de sauvegarde**
Ces exemples montrent comment :

- [Utilisez les options de sauvegarde Diagram](/diagram/fr/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
- [Utilisez les options de sauvegarde PDF](/diagram/fr/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
- [Utilisez les options de sauvegarde HTML](/diagram/fr/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
- [Utiliser les options d'enregistrement d'image](/diagram/fr/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
- [Utilisez les options de sauvegarde SVG](/diagram/fr/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
#### **Utilisation des options de sauvegarde Diagram**
Le code ci-dessous montre comment définir les options d'enregistrement avant d'enregistrer un document au format Visio.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(UseDiagramSaveOptions.class);
// call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Options when saving a diagram into Visio format
DiagramSaveOptions options = new DiagramSaveOptions(SaveFileFormat.VSDX);

// Summary:
/*When characters in the diagram are unicode and not be set with correct font
value or the font is not installed locally, they may appear as block in pdf,
image or XPS.  Set the DefaultFont such as MingLiu or MS Gothic to show these
characters.*/
options.setDefaultFont("MS Gothic");

// Summary:
//   Defines whether need enlarge page to fit drawing content or not.
//   Remarks:
//   Default value is false.
options.setAutoFitPageToDrawingContent(true);
// save diagram
diagram.save(dataDir + "UseDiagramSaveOptions_Out.vsdx", options);

{{< /highlight >}}
```



#### **Utilisation des options de sauvegarde PDF**
The code below shows how to set save options before saving a document to a PDF format.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(UsePDFSaveOptions.class);    
// call the diagram constructor to load diagram from a VSDX file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Options when saving a diagram into the PDF format
PdfSaveOptions options = new PdfSaveOptions();

// discard saving background pages of the Visio diagram
options.setSaveForegroundPagesOnly(true);

// specify the quality of JPEG compression for images (if JPEG compression is used). Default is 95.
options.setJpegQuality(100);

// specify default font name
options.setDefaultFont("Arial");

// conformance level for generated PDF document.
options.setCompliance(PdfCompliance.PDF_15);

// Load the certificate from disk.
// The other constructor overloads can be used to load certificates from different locations.
X509Certificate2 cert = new X509Certificate2(); //"c:\\temp\\certificate.pfx", "feyb4lgcfbme");
// sets a digital signature details. If not set, then no signing will be performed.
options.setDigitalSignatureDetails(new PdfDigitalSignatureDetails(cert, "Test Signing", "Aspose Office", DateTime.getNow(), PdfDigitalSignatureHashAlgorithm.SHA_256));

// set encription details
PdfEncryptionDetails encriptionDetails = new PdfEncryptionDetails("user password", "Owner Password", PdfEncryptionAlgorithm.RC_4_128);
options.setEncryptionDetails(encriptionDetails);
// sets the number of pages to render in PDF.
options.setPageCount(2);
// sets the 0-based index of the first page to render. Default is 0.
options.setPageIndex(0);

// set page size
PageSize pgSize = new PageSize(PaperSizeFormat.A_1);
options.setPageSize(pgSize);
// save in any supported file format
diagram.save(dataDir + "UsePDFSaveOptions_Out.pdf", options);

{{< /highlight >}}
```



#### **Utilisation des options de sauvegarde HTML**
The code below shows how to set save options before saving a document to a HTML format.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(UseHTMLSaveOptions.class);
// call the diagram constructor to load diagram from a VSDX file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Options when saving a diagram into the HTML format
HTMLSaveOptions options = new HTMLSaveOptions();

// Summary:
//   value or the font is not installed locally, they may appear as a block,
//   set the DefaultFont such as MingLiu or MS Gothic to show these
//   characters.
options.setDefaultFont("MS Gothic");
// sets the number of pages to render in HTML.
options.setPageCount(2);
// sets the 0-based index of the first page to render. Default is 0.
options.setPageIndex(0);

// set page size
PageSize pgSize = new PageSize(PaperSizeFormat.A_1);
options.setPageSize(pgSize);
// discard saving background pages of the Visio diagram
options.setSaveForegroundPagesOnly(true);

// Specify whether to save html as a single file, Default value is false.
options.setSaveAsSingleFile(true);

// specify whether to include the toolbar or not. Default value is true.
options.setSaveToolBar(false);
// set title of the HTML document
options.setTitle("Title goes here");

// save in any supported file format
diagram.save(dataDir + "UseHTMLSaveOptions_Out.html", options);

// save resultant HTML directly to a stream
ByteArrayOutputStream dstStream = new ByteArrayOutputStream();
diagram.save(dstStream, SaveFileFormat.HTML);

{{< /highlight >}}
```



#### **Utilisation des options d'enregistrement d'image**
Le code ci-dessous montre comment définir les options d'enregistrement avant d'enregistrer un document dans un format d'image.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(UseImageSaveOptions.class); 
// Call the diagram constructor to load diagram from a VSDX file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

ImageSaveOptions options = new ImageSaveOptions(SaveFileFormat.JPEG);
// specify the quality level to use during compositing.
options.setCompositingQuality(CompositingQuality.HIGH_QUALITY);

// sets the brightness for the the generated images.
// this property has effect only when saving to raster image formats.
//The default value is 0.5. The value must be in the range between 0 and 1.
options.setImageBrightness(1f);

// Summary:
//            value or the font is not installed locally, they may appear as a block,
//            set the DefaultFont such as MingLiu or MS Gothic to show these
//            characters.
options.setDefaultFont("MS Gothic");
// sets the number of pages to render in image.
options.setPageCount(2);
// sets the 0-based index of the first page to render. Default is 0.
options.setPageIndex(0);

// set page size
PageSize pgSize = new PageSize(PaperSizeFormat.A_1);
options.setPageSize(pgSize);
// discard saving background pages of the Visio diagram
options.setSaveForegroundPagesOnly(true);

// sets the color mode for the generated images.
options.setImageColorMode(ImageColorMode.BLACK_AND_WHITE);

// sets the contrast for the generated images.
// this property has effect only when saving to raster image formats.
// the default value is 0.5. The value must be in the range between 0 and 1.
options.setImageContrast(1f);

// specify the algorithm that is used when images are scaled or rotated.
// this property has effect only when saving to raster image formats.
options.setInterpolationMode(InterpolationMode.NEAREST_NEIGHBOR);

// the value may vary from 0 to 100 where 0 means worst quality,
// but maximum compression and 100 means best quality but minimum compression.
// the default value is 95.
options.setJpegQuality(100);

// set a value specifying how pixels are offset during rendering.
options.setPixelOffsetMode(PixelOffsetMode.HIGH_SPEED);

// sets the resolution for the generated images, in dots per inch. The default value is 96.
options.setResolution(2f);

// sets the zoom factor for the generated images.
// the default value is 1.0. The value must be greater than 0.
options.setScale(1f);

// specify whether smoothing (antialiasing) is applied to lines
// and curves and the edges of filled areas.
options.setSmoothingMode(SmoothingMode.HIGH_QUALITY);
// sets the type of compression to apply when saving generated images to the TIFF format.
options.setTiffCompression(TiffCompression.CCITT_3);

// save in any supported file format
diagram.save(dataDir + "UseImageSaveOptions_Out.jpeg", options);

{{< /highlight >}}
```
#### **Utilisation des options de sauvegarde SVG**
Le code ci-dessous montre comment définir les options d'enregistrement avant d'enregistrer un document au format SVG.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(UseSVGSaveOptions.class);
// call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

SVGSaveOptions options = new SVGSaveOptions();

// Summary:
//     value or the font is not installed locally, they may appear as a block,
//     set the DefaultFont such as MingLiu or MS Gothic to show these
//     characters.
options.setDefaultFont("MS Gothic");
// sets the 0-based index of the first page to render. Default is 0.
options.setPageIndex(0);

// set page size
PageSize pgSize = new PageSize(PaperSizeFormat.A_1);
options.setPageSize(pgSize);

diagram.save(dataDir + "UseSVGSaveOptions_Out.svg", options);

{{< /highlight >}}
```
