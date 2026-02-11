---
title: Сохранить документ Visio программно
linktitle: Сохранить документ Visio
type: docs
weight: 30
url: /ru/net/save-visio-document/
description: На этой странице описывается, как сохранить документ Visio в файл, поток с библиотекой Aspose.Diagram.
---
## **Visio Обзор сохранения чертежа**
 Использовать[Diagram.Save]() метод сохранения чертежа Microsoft Visio. Есть перегрузки, позволяющие сохранить рисунок в файл. Чертеж можно сохранить в любом формате сохранения, поддерживаемом Aspose.Diagram. Список всех поддерживаемых форматов сохранения см.[СохранитьФайлФормат]() перечисление.
## **Сохранение Visio Diagram**
 Класс Diagram класса Aspose.Diagram API представляет чертеж Visio, и разработчики могут сохранять его объект Visio diagram в любом поддерживаемом формате файла. Чтобы сохранить файл Microsoft Visio, просто используйте[Diagram.Save]()метод, он принимает имя файла с полным путем или объект файлового потока. Aspose.Diagram API выводит формат сохранения из расширения файла, а также предлагает дополнительный параметр SaveFileFormat для указания формата выходного файла.
### **Сохраните Visio Diagram в любом поддерживаемом формате файла**
Используя Aspose.Diagram API, разработчики могут сохранить Visio diagram в любом поддерживаемом формате файла, как указано ниже:
**VSDX, VSDM, VSSX, VSSM, VSTX, VSTM, VDX, VSX, VTX, TIFF, PNG, BMP, EMF, JPEG, PDF, XPS, GIF, HTML, SVG, SWF and XAML**
### **Сохранение Diagram Пример программирования**
В приведенном ниже примере документ сохраняется в файл.

{{< highlight "java" >}}

 // Save a Visio diagram

diagram.Save(GetMyDir() + "MyOutput.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
## **Указание Visio параметров сохранения**
 Есть несколько[Diagram.Save]()перегрузки методов, которые принимают объект SaveOptions. Это должен быть объект класса, производного от класса SaveOptions. У каждого формата сохранения есть соответствующий класс, который содержит параметры сохранения для этого формата сохранения. Например, есть PdfSaveOptions для формата сохранения SaveFileFormat.PDF.
### **Visio Diagram Параметры сохранения**
Эти примеры показывают, как:

- [Используйте параметры сохранения Diagram](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Используйте параметры сохранения PDF](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Используйте параметры сохранения HTML](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Используйте параметры сохранения изображения](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Используйте параметры сохранения SVG](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Используйте параметры сохранения SWF](https://docs.aspose.com/diagram/net/save-visio-document/).
#### **Использование параметров сохранения Diagram**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением документа в формате Visio.

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



#### **Использование параметров сохранения PDF**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением документа в формате PDF.

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



#### **Использование параметров сохранения HTML**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением документа в формате файла HTML.

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



#### **Использование параметров сохранения изображения**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением документа в формате файла изображения.



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


Использование параметров сохранения SVG

В приведенном ниже коде показано, как установить параметры сохранения перед сохранением документа в формате SVG.

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


Использование параметров сохранения SWF

В приведенном ниже коде показано, как установить параметры сохранения перед сохранением документа в формате SWF.

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

Иногда разработчикам необходимо программно сохранять или экспортировать диаграммы Visio в различные форматы файлов (например, VDX, PDF, JPEG и т. д.).
## **Сохранить файл VSD в различных форматах файлов (VDX, PDF и JPEG)**
 В этой статье приведен пример кода, иллюстрирующий использование[ВСТО](https://docs.aspose.com/diagram/net/save-visio-document/) а также[Aspose.Diagram for .NET](https://docs.aspose.com/diagram/net)чтобы программно сохранить файл Microsoft Visio VSD в файл VDX, файл PDF или файл JPEG. Ниже приведены параллельные фрагменты кода для VSTO и Aspose.Diagram for .NET, в которых объясняется, как сохранить файл VSD в различных форматах файлов. Вы заметите, что код Aspose.Diagram короче. Не стесняйтесь использовать код и изменять его в соответствии с вашими конкретными потребностями.
### **Сохранение файла VSD в другие форматы с помощью VSTO**
VSTO позволяет программировать Microsoft Visio файлов. Чтобы сохранить файл в другом формате:

1. Создайте объект приложения Visio.
1. Сделать объект приложения невидимым.
1. Загрузите diagram.
1. Сохранить в VDX, PDF и JPEG.
1. Закройте объект приложения Visio.
#### **Сохранение файла VSD с помощью примера программирования VSTO**
{{% alert color="primary" %}} 

используя Visio = Microsoft.Office.Interop.Visio;
Импорт Visio = Microsoft.Office.Interop.Visio

{{% /alert %}} 

**Пример:**

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
### ` `**Сохранение файла VSD в другие форматы с помощью Aspose.Diagram for .NET**
Используя Aspose.Diagram, разработчикам не нужно Microsoft Office Visio в машине, и они могут работать независимо от Microsoft Office Автоматизация.

Фрагменты кода ниже показывают, как:

1. Загрузите diagram.
1. Сохраните diagram в VSX, PDF и JPEG.
#### **Сохранение файла VSD с образцом программы Aspose.Diagram for .NET**
{{% alert color="primary" %}} 

используя Aspose.Diagram;
Импорт Aspose.Diagram

{{% /alert %}} 

**Пример:**

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
