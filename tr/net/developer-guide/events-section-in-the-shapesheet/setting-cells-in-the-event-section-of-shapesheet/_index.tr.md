---
title: ShapeSheet'in Olay Bölümünde Hücreleri Ayarlama
type: docs
weight: 10
url: /tr/net/setting-cells-in-the-event-section-of-shapesheet/
description: visio dosyalarının olay özelliklerini yönetin.
---
{{% alert color="primary" %}} 

Geliştiriciler, Aspose.Diagram API'i kullanarak, olayları otomatik olarak işleyen Visio formülleri yazarak bir şeklin belirli kullanıcı eylemlerine nasıl yanıt vereceğini tanımlayabilir. Kullanıcı aşağıda açıklanan dört eylemden birini gerçekleştirdiğinde, karşılık gelen ShapeSheet hücresindeki formül değerlendirilir.

- **Metin** - Bir şeklin metni veya metin bileşimi değiştiğinde değerlendirilen bir olay öğesi.
- **EventXFMod** - Şeklin sayfadaki konumu, boyutu veya yönü değiştirilir.
- **EventDblClick** - Şekil çift tıklanır.
- **EventDrop** Bir şekli yapıştırarak, çoğaltarak veya sürükleyerek ya da bir ana kopyayı sürükleyip bırakarak yeni bir örnek oluşturulur.
- **EventMultiDrop** - bir şekli yapıştırarak, çoğaltarak veya sürükleyerek ya da bir ana kopyayı sürükleyip bırakarak birden çok yeni örnek oluşturulduğunda.
- **Veri** - Gelecekte kullanılmak üzere rezerve edilmiştir.

{{% /alert %}} 
## **Olay Hücrelerini Ayarlama**
[Etkinlik](https://reference.aspose.com/diagram/net/aspose.diagram/event) class, geliştiricilerin ShapeSheet'te olay hücreleri ayarlamasına olanak tanır. Bu yardım konusu, geliştiricilerin olay hücrelerinde formülleri nasıl ayarlayabileceklerini gösterir:

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_EventSection();

// Load diagram
Diagram diagram = new Diagram(dataDir + "TestTemplate.vsdm");
// Get page
Aspose.Diagram.Page page = diagram.Pages.GetPage(0);
// Get shape id
long shapeId = page.AddShape(3.0, 3.0, 0.36, 0.36, "Square");
// Get shape
Aspose.Diagram.Shape shape = page.Shapes.GetShape(shapeId);

// Set event cells in the ShapeSheet
shape.Event.EventXFMod.Ufe.F = "CALLTHIS(\"ThisDocument.ShowAlert\")";
shape.Event.EventDblClick.Ufe.F = "CALLTHIS(\"ThisDocument.ShowAlert\")";
shape.Event.EventDrop.Ufe.F = "CALLTHIS(\"ThisDocument.ShowAlert\")";
shape.Event.EventMultiDrop.Ufe.F = "CALLTHIS(\"ThisDocument.ShowAlert\")";
shape.Event.TheText.Ufe.F = "CALLTHIS(\"ThisDocument.ShowAlert\")";
shape.Event.TheData.Ufe.F = "CALLTHIS(\"ThisDocument.ShowAlert\")";

// Save diagram
diagram.Save(dataDir + "SettingCellsInEventSection_out.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}
```
