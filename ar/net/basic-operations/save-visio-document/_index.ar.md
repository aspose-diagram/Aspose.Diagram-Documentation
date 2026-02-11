---
title: احفظ Visio الوثيقة برمجيا
linktitle: احفظ الوثيقة Visio
type: docs
weight: 30
url: /ar/net/save-visio-document/
description: تصف هذه الصفحة كيفية حفظ Visio مستند إلى ملف ، دفق باستخدام مكتبة Aspose.Diagram.
---
## **Visio نظرة عامة على حفظ الرسم**
 استخدم ال[Diagram.Save]() طريقة لحفظ رسم Microsoft Visio. هناك حمولات زائدة تسمح بحفظ رسم في ملف. يمكن حفظ الرسم بأي تنسيق حفظ يدعمه Aspose.Diagram. للحصول على قائمة بجميع تنسيقات الحفظ المدعومة ، راجع ملف[SaveFileFormat]() تعداد.
## **توفير Visio Diagram**
 تمثل الفئة Diagram من Aspose.Diagram API رسمًا Visio ويمكن للمطورين حفظ كائن Visio diagram بأي تنسيق ملف مدعوم. لحفظ ملف Microsoft Visio ، ما عليك سوى استخدام ملحق[Diagram.Save]()الأسلوب ، فإنه يقبل اسم ملف بمسار كامل أو كائن دفق ملف. يستنتج Aspose.Diagram API تنسيق الحفظ من امتداد الملف ويقدم أيضًا معامل SaveFileFormat إضافيًا لتحديد تنسيق ملف الإخراج.
### **احفظ Visio Diagram بأي تنسيق ملف مدعوم**
باستخدام Aspose.Diagram API ، يمكن للمطورين حفظ Visio diagram بأي تنسيق ملف مدعوم كما هو موضح أدناه:
**VSDX و VSDM و VSSX و VSSM و VSTX و VSTM و VDX و VSX و VTX و TIFF و PNG و BMP و EMF و JPEG و 07611531183 و EMF و 07611331183 و EMF و JPEG**
### **حفظ Diagram عينة البرمجة**
المثال أدناه يحفظ مستندًا إلى ملف.

{{< highlight "java" >}}

 // Save a Visio diagram

diagram.Save(GetMyDir() + "MyOutput.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
## **تحديد Visio خيارات الحفظ**
 هناك العديد[Diagram.Save]() الأسلوب الزائد الذي يقبل كائن SaveOptions. يجب أن يكون هذا كائنًا من فئة مشتقة من فئة SaveOptions. يحتوي كل تنسيق حفظ على فئة مقابلة تحتوي على خيارات الحفظ لتنسيق الحفظ هذا. على سبيل المثال ، هناك PdfSaveOptions لتنسيق حفظ SaveFileFormat.PDF.
### **Visio Diagram حفظ الخيارات**
توضح هذه الأمثلة كيفية:

- [استخدم Diagram حفظ الخيارات](https://docs.aspose.com/diagram/net/save-visio-document/).
- [استخدم PDF حفظ الخيارات](https://docs.aspose.com/diagram/net/save-visio-document/).
- [استخدم HTML حفظ الخيارات](https://docs.aspose.com/diagram/net/save-visio-document/).
- [استخدم خيارات حفظ الصورة](https://docs.aspose.com/diagram/net/save-visio-document/).
- [استخدم SVG حفظ الخيارات](https://docs.aspose.com/diagram/net/save-visio-document/).
- [استخدم SWF حفظ الخيارات](https://docs.aspose.com/diagram/net/save-visio-document/).
#### **استخدام Diagram حفظ الخيارات**
يوضح الكود أدناه كيفية تعيين خيارات الحفظ قبل حفظ المستند بتنسيق Visio.

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



#### **استخدام PDF حفظ الخيارات**
يوضح الكود أدناه كيفية تعيين خيارات الحفظ قبل حفظ مستند بتنسيق PDF.

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



#### **استخدام HTML حفظ الخيارات**
يوضح الكود أدناه كيفية تعيين خيارات الحفظ قبل حفظ مستند بتنسيق ملف HTML.

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



#### **استخدام خيارات حفظ الصورة**
يوضح الكود أدناه كيفية تعيين خيارات الحفظ قبل حفظ مستند بتنسيق ملف الصورة.



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


استخدام SVG حفظ الخيارات

يوضح الكود أدناه كيفية تعيين خيارات الحفظ قبل حفظ المستند بتنسيق SVG.

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


استخدام SWF حفظ الخيارات

يوضح الكود أدناه كيفية تعيين خيارات الحفظ قبل حفظ المستند بتنسيق SWF.

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

في بعض الأحيان ، يحتاج المطورون إلى حفظ الرسوم التخطيطية Visio أو تصديرها إلى تنسيقات ملفات مختلفة برمجيًا (مثل VDX و PDF و JPEG وما إلى ذلك).
## **حفظ VSD الملف بتنسيقات ملفات مختلفة (VDX و PDF و JPEG)**
 توفر هذه المقالة مثال رمز يوضح كيفية الاستخدام[VSTO](https://docs.aspose.com/diagram/net/save-visio-document/) و[Aspose.Diagram for .NET](https://docs.aspose.com/diagram/net)لحفظ ملف Microsoft Visio VSD في ملف VDX أو ملف PDF أو ملف JPEG برمجيًا. فيما يلي مقتطفات التعليمات البرمجية المتوازية لـ VSTO و Aspose.Diagram for .NET التي تشرح كيفية حفظ ملف VSD في تنسيقات ملفات مختلفة. ستلاحظ أن كود Aspose.Diagram أقصر. لا تتردد في استخدام الرمز وتغييره لتلبية احتياجاتك الخاصة.
### **حفظ ملف VSD إلى تنسيقات أخرى باستخدام VSTO**
يتيح لك VSTO البرمجة باستخدام ملفات Microsoft Visio. لحفظ ملف بتنسيقات أخرى:

1. قم بتكوين عنصر تطبيق Visio.
1. جعل كائن التطبيق غير مرئي.
1. قم بتحميل diagram.
1. احفظ إلى VDX و PDF و JPEG.
1. قم بإنهاء كائن التطبيق Visio.
#### **حفظ ملف VSD باستخدام نموذج برمجة VSTO**
{{% alert color="primary" %}} 

باستخدام Visio = Microsoft.Office.Interop.Visio ؛
الواردات Visio = Microsoft.Office.Interop.Visio

{{% /alert %}} 

**مثال:**

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
### ` `**حفظ VSD الملف إلى تنسيقات أخرى باستخدام Aspose.Diagram for .NET**
باستخدام Aspose.Diagram ، لا يحتاج المطورون إلى Microsoft Office Visio في الجهاز ، ويمكنهم العمل بشكل مستقل عن Microsoft Office Automation.

توضح مقتطفات التعليمات البرمجية أدناه كيفية:

1. قم بتحميل diagram.
1. احفظ diagram إلى VSX و PDF و JPEG.
#### **حفظ VSD ملف باستخدام عينة برمجة Aspose.Diagram for .NET**
{{% alert color="primary" %}} 

باستخدام Aspose.Diagram ؛
الواردات Aspose.Diagram

{{% /alert %}} 

**مثال:**

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
