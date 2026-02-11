---
title: Katman Özelliklerini Değiştir
type: docs
weight: 130
url: /tr/net/change-properties-layer/
description: Bu bölümde, katman özelliklerinin Aspose.Diagram ile nasıl değiştirileceği açıklanmaktadır.
---
## **Visio'de Katman Özelliklerini Değiştirin**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) Microsoft Office Visio diagram'de katman özelliklerini değiştirmeye izin verir. Her şekil birden çok katmana ait olabilir, böylece geliştiriciler katmanın özelliklerini son kullanıcı ihtiyaçlarına göre değiştirebilir. bu[Sayfa Sayfası](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet)class nesnesi, Visio çiziminde katman nesneleri eklemeye ve kaldırmaya izin veren Katmanlar sunar. Kullanıcılar yönetebilir[Katman](https://reference.aspose.com/diagram/net/aspose.diagram/layer) özellikleri aşağıdaki gibi Aspose.Diagram API kullanarak programlı olarak:
### **Katman Özelliklerini Değiştirme Programlama Örneği**
Aşağıdaki kod parçası, katmanın özelliklerini değiştirmeye yardımcı olur.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Layers();

// Load a source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");

// Iterate through the layers
foreach (Aspose.Diagram.Layer layer in Page.PageSheet.Layers)
{
    layer.Visible.Value = Aspose.Diagram.BOOL.True;
    layer.Print.Value = Aspose.Diagram.BOOL.True;
}
// Save diagram
diagram.Save(dataDir + "ChangeLayerProperty_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```