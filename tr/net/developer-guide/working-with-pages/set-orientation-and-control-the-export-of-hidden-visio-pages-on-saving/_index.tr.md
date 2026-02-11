---
title: Yönlendirmeyi Ayarlayın ve Kaydederken Gizli Visio Sayfalarının Dışa Aktarılmasını Kontrol Edin
type: docs
weight: 20
url: /tr/net/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/
description: Bu bölümde sayfa düzeninin Aspose.Diagram ile nasıl ayarlanacağı açıklanmaktadır.
---
## **Visio Sayfa Düzenini Dikey veya Yatay olarak değiştirme**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API, geliştiricilerin Visio çizim sayfasının yönünü programlı olarak ayarlamasına olanak tanır. Bu yardım konusu, bu görevin nasıl gerçekleştirileceğini açıklar.

 Aspose.Diagram for .NET API'de var[Sayfa](http://www.aspose.com/api/net/diagram/aspose.diagram/page) Visio çizim sayfasını temsil eden sınıf. Page sınıfı tarafından sunulan PageSheet özelliği ayrıca yazdırma özelliklerini de gösterir. Yazdırma özelliklerinin PrintPageOrientation alanı, sayfayı döndürmeye izin verir. Dikey, Yatay ve yazıcıdaki ile aynı olmak üzere üç seçenek sunar. PrintPageOrientation alanı, Aspose.Diagram API kullanılarak programlı olarak ayarlanabilir.

Bu örnek şu şekilde çalışır:

1. Mevcut bir Visio diagram'i Diagram sınıf nesnesine yükleyin.
1. Visio sayfasını ayıklayın
1. Yönünü Dikey, Yatay veya yazıcıdakiyle aynı olarak ayarlayın.
1. Visio diagram'i kaydedin.
### **Oryantasyon Programlama Örneği Ayarla**
Aşağıdaki kod örneği, Visio sayfasının yönünün nasıl ayarlanacağını gösterir.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Flow 1");
// Page orientation
page.PageSheet.PrintProps.PrintPageOrientation.Value = PrintPageOrientationValue.Landscape;
// Save Visio
diagram.Save(dataDir + "SetPageOrientation_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Kaydederken Gizli Visio Sayfalarının Dışa Aktarılmasını Kontrol Edin**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/)API, geliştiricilerin diagram'i PDF, HTML, Resim (PNG, JPEG, GIF), SVG ve XPS dosyalarına kaydederken gizli Visio sayfalarını dahil etmesine veya hariç tutmasına olanak tanır. Hatta Aspose.Diagram API'i kullanarak Visio sayfayı gizleyebilirler çünkü seçeneği ShapeSheet sayfasındaki UIVisibility hücresi aracılığıyla zaten mevcuttur.
### **Visio Diagram'de bir Sayfayı Gizle ve Dışa Aktarma Seçeneğini Ayarla**
 Aspose.Diagram for .NET API'de var[Sayfa](http://www.aspose.com/api/net/diagram/aspose.diagram/page) Visio çizim sayfasını temsil eden sınıf. Page sınıfı tarafından sunulan PageSheet özelliği, sayfa özelliklerini de gösterir. Sayfa özelliklerinin UIVisibility alanı, sayfanın gizlenmesine olanak tanır. Geliştiriciler daha sonra SVGSaveOptions, XPSSaveOptions, ImageSaveOptions, HTMLSaveOptions ve PdfSaveOptions sınıflarına eklenen ExportHiddenPage özelliğini kullanabilir.
#### **PDF için Dışa Aktarma Seçeneğini ayarlayın**
Aşağıdaki kod, diagram - PDF biçimini kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// Load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get a particular page
Page page = diagram.Pages.GetPage("Flow 2");
// Set Visio page visiblity
page.PageSheet.PageProps.UIVisibility.Value = BOOL.True;

// Initialize PDF save options
PdfSaveOptions options = new PdfSaveOptions();
// Set export option of hidden Visio pages
options.ExportHiddenPage = false;

// Save the Visio diagram
diagram.Save(dataDir + "ExportOfHiddenVisioPagesToPDF_out.pdf", options);

{{< /highlight >}}

#### **HTML için Dışa Aktarma Seçeneğini ayarlayın**
Aşağıdaki kod, diagram - HTML biçimini kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// Load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get a particular page
Page page = diagram.Pages.GetPage("Flow 2");
// Set Visio page visiblity
page.PageSheet.PageProps.UIVisibility.Value = UIVisibilityValue.Visible;

// Initialize PDF save options
HTMLSaveOptions options = new HTMLSaveOptions();
// Set export option of hidden Visio pages
options.ExportHiddenPage = false;
// Set export option of comments
options.IsExportComments = false;

// Save the Visio diagram
diagram.Save(dataDir + "ExportOfHiddenVisioPagesToHTML_out.html", options);

{{< /highlight >}}

#### **Görüntü için Dışa Aktarma Seçeneğini Ayarlayın**
Aşağıdaki kod, bir diagram'i görüntü formatına kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// Load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get a particular page
Page page = diagram.Pages.GetPage("Flow 2");
// Set Visio page visiblity
page.PageSheet.PageProps.UIVisibility.Value = UIVisibilityValue.Visible;

// Initialize PDF save options
ImageSaveOptions options = new ImageSaveOptions(SaveFileFormat.JPEG);
// Set export option of hidden Visio pages
options.ExportHiddenPage = false;
// Set export option of comments
options.IsExportComments = false;

// Save the Visio diagram
diagram.Save(dataDir + "ExportOfHiddenVisioPagesToImage_out.jpeg", options);

{{< /highlight >}}

#### **SVG için Dışa Aktarma Seçeneğini ayarlayın**
Aşağıdaki kod, diagram - SVG biçimini kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// Load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get a particular page
Page page = diagram.Pages.GetPage("Flow 2");
// Set Visio page visiblity
page.PageSheet.PageProps.UIVisibility.Value = UIVisibilityValue.Visible;

// Initialize PDF save options
SVGSaveOptions options = new SVGSaveOptions();
// Set export option of hidden Visio pages
options.ExportHiddenPage = false;
// Set export guide shapes 
options.ExportGuideShapes = false;
// Set save format
options.SaveFormat = Aspose.Diagram.SaveFileFormat.SVG;
// Set SVG fit to view port
options.SVGFitToViewPort = true;
// Set export element as Rectangle
options.ExportElementAsRectTag = true;


// Save the Visio diagram
diagram.Save(dataDir + "ExportOfHiddenVisioPagesToSVG_out.svg", options);

{{< /highlight >}}

#### **XPS için Dışa Aktarma Seçeneğini ayarlayın**
Aşağıdaki kod, diagram - XPS biçimini kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// Load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get a particular page
Page page = diagram.Pages.GetPage("Flow 2");
// Set Visio page visiblity
page.PageSheet.PageProps.UIVisibility.Value = BOOL.True;

// Initialize PDF save options
XPSSaveOptions options = new XPSSaveOptions();
// Set export option of hidden Visio pages
options.ExportHiddenPage = false;

// Save the Visio diagram
diagram.Save(dataDir + "ExportOfHiddenVisioPagesToXPS_out.xps", options);

{{< /highlight >}}

