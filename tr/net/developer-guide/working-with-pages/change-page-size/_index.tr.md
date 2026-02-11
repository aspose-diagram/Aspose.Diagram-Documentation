---
title: Sayfa Boyutunu Değiştir
type: docs
weight: 10
url: /tr/net/change-page-size/
description: Bu bölümde, visio dosyasındaki sayfa boyutunun Aspose.Diagram ile nasıl değiştirileceği açıklanmaktadır.
---
## **Sayfa Boyutunu Değiştir**

 bu[Sayfa](http://www.aspose.com/api/net/diagram/aspose.diagram/page)nesne, ön plan sayfasının veya arka plan sayfasının çizim alanını temsil eder. Tarafından sunulan Pages özelliği[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class, Aspose.Diagram.Page nesnelerinin koleksiyonunu destekler.
 bu[Sayfa Destekleri](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/pageprops) nesne, sayfa genişliği, yüksekliği ve ölçeği gibi sayfa niteliklerini temsil eder. Bu özellik, sayfa boyutunu değiştirmek için kullanılabilir.

Sayfa boyutunu değiştirmek için PageProps özelliğini kullanın.
### **Sayfa Boyutunu Ayarla Programlama Örneği**
Aşağıdaki kod parçası, sayfa boyutunu diagram'den değiştirir.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Flow 1");
// Set Page Size
page.PageSheet.PageProps.PageHeight.Value = 8;
page.PageSheet.PageProps.PageWidth.Value = 11;

// Save Visio
diagram.Save(dataDir + "SetPageSize_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

