---
title: Sayfa Boyutunu Değiştir
type: docs
weight: 10
url: /tr/java/change-page-size/
description: Bu bölümde, visio dosyasındaki sayfa boyutunun Aspose.Diagram ile nasıl değiştirileceği açıklanmaktadır.
---
## **Sayfa Boyutunu Değiştir**

 bu[Sayfa](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)nesne, ön plan sayfasının veya arka plan sayfasının çizim alanını temsil eder. Tarafından sunulan Pages özelliği[Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/diagram) class, Aspose.Diagram.Page nesnelerinin koleksiyonunu destekler.
 bu[Sayfa Destekleri](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageProps) nesne, sayfa genişliği, yüksekliği ve ölçeği gibi sayfa niteliklerini temsil eder. Bu özellik, sayfa boyutunu değiştirmek için kullanılabilir.

Sayfa boyutunu değiştirmek için PageProps özelliğini kullanın.
### **Sayfa Boyutunu Ayarla Programlama Örneği**
Aşağıdaki kod parçası, sayfa boyutunu diagram'den değiştirir.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ChangeVisioPageSize.class);
      
// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Page page = diagram.getPages().getPage("Flow 1");
// Set Page Size
page.getPageSheet().getPageProps().getPageHeight().setValue(8);
page.getPageSheet().getPageProps().getPageWidth().setValue(11);

// Save Visio
diagram.save(dataDir + "SetPageSize_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

