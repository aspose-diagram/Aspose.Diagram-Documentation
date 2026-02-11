---
title: Sayfa Otomatik Genişletmeyi Kontrol Et
type: docs
weight: 10
url: /tr/java/check-page-autoexpand/
description: Bu bölüm, Aspose.Diagram ile bir visio dosyasında sayfanın otomatik olarak nasıl genişletileceğini kontrol etmeyi veya değiştirmeyi açıklar.
---
## **Kontrol sayfası Otomatik Genişletme**

 bu[Sayfa](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)nesne, ön plan sayfasının veya arka plan sayfasının çizim alanını temsil eder. Tarafından sunulan Pages özelliği[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) class, Aspose.Diagram.Page nesnelerinin koleksiyonunu destekler.
 bu[Sayfa Destekleri](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageProps) nesne, sayfa genişliği, yüksekliği ve ölçeği gibi sayfa niteliklerini temsil eder. Bu özellik, sayfanın otomatik genişletilmesini kontrol etmek için kullanılabilir.

Sayfanın otomatik genişletilmesini kontrol etmek için PageProps özelliğini kullanın.
### **Kontrol Sayfası Otomatik Genişletme Programlama Örneği**
Aşağıdaki kod parçası kontrol sayfası, diagram'den otomatik olarak genişliyor.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CheckChangeAutoExpand.class);
      
// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Page page = diagram.getPages().getPage("Page-2");
// Get Page autoexpand
boolean isAutoExpand = page.getPageSheet().getPageProps().getDrawingResizeType().getValue() == DrawingResizeTypeValue.AUTOMATICALLY ? true : false;
//Set Page autoexpand
page.getPageSheet().getPageProps().getDrawingResizeType().setValue(DrawingResizeTypeValue.NOT_AUTOMATICALLY);

// Save Visio
diagram.save(dataDir + "SetAutoExpand_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

