---
title: Yönlendirmeyi Ayarlayın ve Kaydederken Gizli Visio Sayfalarının Dışa Aktarılmasını Kontrol Edin
type: docs
weight: 20
url: /tr/java/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/
---
## **Visio Sayfa Düzenini Dikey veya Yatay olarak değiştirme**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API, geliştiricilerin Visio çizim sayfasının yönünü programlı olarak ayarlamasına olanak tanır. Bu yardım konusu, bu görevin nasıl gerçekleştirileceğini açıklar.

 Aspose.Diagram for Java API'de var[Sayfa](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) Visio çizim sayfasını temsil eden sınıf. Page sınıfı tarafından sunulan PageSheet özelliği ayrıca yazdırma özelliklerini de gösterir. Yazdırma özelliklerinin PrintPageOrientation alanı, sayfayı döndürmeye izin verir. Dikey, Yatay ve yazıcıdaki ile aynı olmak üzere üç seçenek sunar. PrintPageOrientation alanı, Aspose.Diagram API kullanılarak programlı olarak ayarlanabilir.

Bu örnek şu şekilde çalışır:

1. Mevcut bir Visio diagram'i Diagram sınıf nesnesine yükleyin.
1. Visio sayfasını ayıklayın
1. Yönünü Dikey, Yatay veya yazıcıdakiyle aynı olarak ayarlayın.
1. Visio diagram'i kaydedin.
### **Oryantasyon Programlama Örneği Ayarla**
Aşağıdaki kod örneği, Visio sayfasının yönünün nasıl ayarlanacağını gösterir.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetVisioPageOrientation.class);  
// initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get Visio page
Page page = diagram.getPages().getPage("Flow 1");
// page orientation
page.getPageSheet().getPrintProps().getPrintPageOrientation().setValue(PrintPageOrientationValue.LANDSCAPE);
// save Visio
diagram.save(dataDir + "SetPageOrientation_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Kaydederken Gizli Visio Sayfalarının Dışa Aktarılmasını Kontrol Edin**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/)API, geliştiricilerin diagram'i PDF, HTML, Resim (PNG, JPEG, GIF), SVG ve XPS dosyalarına kaydederken gizli Visio sayfalarını dahil etmesine veya hariç tutmasına olanak tanır. Hatta Aspose.Diagram API'i kullanarak Visio sayfayı gizleyebilirler çünkü seçeneği ShapeSheet sayfasındaki UIVisibility hücresi aracılığıyla zaten mevcuttur.
### **Visio Diagram'de bir Sayfayı Gizle ve Dışa Aktarma Seçeneğini Ayarla**
 Aspose.Diagram for Java API'de var[Sayfa](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) Visio çizim sayfasını temsil eden sınıf. Page sınıfı tarafından sunulan PageSheet özelliği, sayfa özelliklerini de gösterir. Sayfa özelliklerinin UIVisibility alanı, sayfanın gizlenmesine olanak tanır. Geliştiriciler daha sonra SVGSaveOptions, XPSSaveOptions, ImageSaveOptions, HTMLSaveOptions ve PdfSaveOptions sınıflarına eklenen ExportHiddenPage özelliğini kullanabilir.
#### **PDF için Dışa Aktarma Seçeneğini ayarlayın**
Aşağıdaki kod, diagram - PDF biçimini kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExporToHiddenVisioPagesToPdf.class);  
        
// load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a particular page
Page page = diagram.getPages().getPage("Flow 2");
// set Visio page visiblity
page.getPageSheet().getPageProps().getUIVisibility().setValue(BOOL.TRUE);

// initialize PDF save options
PdfSaveOptions options = new PdfSaveOptions();
// set export option of hidden Visio pages
options.setExportHiddenPage(false);

//Save the Visio diagram
diagram.save(dataDir + "ExportOfHiddenVisioPagesToPDF_Out.pdf", options);

{{< /highlight >}}
```
#### **HTML için Dışa Aktarma Seçeneğini ayarlayın**
Aşağıdaki kod, diagram - HTML biçimini kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(ExportOfHiddenVisioPagesToHtml.class) + "Pages/";

// load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a particular page
Page page = diagram.getPages().getPage("Flow 2");
// set Visio page visiblity
page.getPageSheet().getPageProps().getUIVisibility().setValue(BOOL.TRUE);

// initialize PDF save options
HTMLSaveOptions options = new HTMLSaveOptions();
// set export option of hidden Visio pages
options.setExportHiddenPage(false);
// set export option of comments
options.setExportComments(false);
// Save the Visio diagram
diagram.save(dataDir + "ExportOfHiddenVisioPagesToHTML_Out.html", options);

{{< /highlight >}}
```
#### **Görüntü için Dışa Aktarma Seçeneğini Ayarlayın**
Aşağıdaki kod, bir diagram'i görüntü formatına kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(ExportOfHiddenVisioPagesToImage.class) + "Pages/";

// load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a particular page
Page page = diagram.getPages().getPage("Flow 2");
// set Visio page visiblity
page.getPageSheet().getPageProps().getUIVisibility().setValue(BOOL.TRUE);
// initialize PDF save options
ImageSaveOptions options = new ImageSaveOptions(SaveFileFormat.JPEG);
// set export option of hidden Visio pages
options.setExportHiddenPage(false);
// set export option of comments
options.setExportComments(false);

// Save the Visio diagram
diagram.save(dataDir + "ExportOfHiddenVisioPagesToImage_Out.jpeg", options);

{{< /highlight >}}
```
#### **SVG için Dışa Aktarma Seçeneğini ayarlayın**
Aşağıdaki kod, diagram - SVG biçimini kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(ExportOfHiddenVisioPagesToSVG.class) + "Pages/";

// load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a particular page
Page page = diagram.getPages().getPage("Flow 2");
// set Visio page visiblity
page.getPageSheet().getPageProps().getUIVisibility().setValue(BOOL.TRUE);

// initialize PDF save options
SVGSaveOptions options = new SVGSaveOptions();
// set export option of hidden Visio pages
options.setExportHiddenPage(false);
// Set SVG fit to view port
options.setSVGFitToViewPort(true);
// Set export element as Rectangle
options.setExportElementAsRectTag(true);

// save the Visio diagram
diagram.save(dataDir + "ExportOfHiddenVisioPagesToSVG_Out.svg", options);

{{< /highlight >}}
```
