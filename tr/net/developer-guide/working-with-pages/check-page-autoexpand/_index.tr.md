---
title: Sayfa Otomatik Genişletmeyi Kontrol Et
type: docs
weight: 10
url: /tr/net/check-page-autoexpand/
description: Bu bölüm, Aspose.Diagram ile bir visio dosyasında sayfanın otomatik olarak nasıl genişletileceğini kontrol etmeyi veya değiştirmeyi açıklar.
---
## **Sayfa Boyutunu Değiştir**

 bu[Sayfa](http://www.aspose.com/api/net/diagram/aspose.diagram/page)nesne, ön plan sayfasının veya arka plan sayfasının çizim alanını temsil eder. Tarafından sunulan Pages özelliği[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class, Aspose.Diagram.Page nesnelerinin koleksiyonunu destekler.
 bu[Sayfa Destekleri](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/pageprops) nesne, sayfa genişliği, yüksekliği ve ölçeği gibi sayfa niteliklerini temsil eder. Bu özellik, sayfanın otomatik genişletilmesini kontrol etmek için kullanılabilir.

Sayfanın otomatik genişletilmesini kontrol etmek için PageProps özelliğini kullanın.
### **Sayfa Boyutunu Ayarla Programlama Örneği**
Aşağıdaki kod parçası kontrol sayfası, diagram'den otomatik olarak genişliyor.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Flow 1");
// Get Page autoexpand
bool isAutoExpand = page.PageSheet.PageProps.DrawingResizeType.Value == DrawingResizeTypeValue.Automatically ? true : false;
//Set Page autoexpand
page.PageSheet.PageProps.DrawingResizeType.Value = DrawingResizeTypeValue.NotAutomatically;

// Save Visio
diagram.Save(dataDir + "SetAutoExpand_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

