---
title: ShapeSheet'in Olay Bölümünde Hücreleri Ayarlama
type: docs
weight: 10
url: /tr/java/setting-cells-in-the-event-section-of-shapesheet/
---
{{% alert color="primary" %}} 

Geliştiriciler, Aspose.Diagram API'i kullanarak, olayları otomatik olarak işleyen Visio formülleri yazarak bir şeklin belirli kullanıcı eylemlerine nasıl yanıt vereceğini tanımlayabilir. Kullanıcı aşağıda açıklanan eylemlerden birini gerçekleştirdiğinde, karşılık gelen ShapeSheet hücresindeki formül değerlendirilir.

- **Metin** - Bir şeklin metni veya metin bileşimi değiştiğinde değerlendirilen bir olay öğesi.
- **EventXFMod** - Şeklin sayfadaki konumu, boyutu veya yönü değiştirilir.
- **EventDblClick** - Şekil çift tıklanır.
- **EventDrop** Bir şekli yapıştırarak, çoğaltarak veya sürükleyerek ya da bir ana kopyayı sürükleyip bırakarak yeni bir örnek oluşturulur.
- **EventMultiDrop** - bir şekli yapıştırarak, çoğaltarak veya sürükleyerek ya da bir ana kopyayı sürükleyip bırakarak birden çok yeni örnek oluşturulduğunda.
- **Veri** - Gelecekte kullanılmak üzere rezerve edilmiştir.

{{% /alert %}} 
## **Olay Hücrelerini Ayarlama**
[Etkinlik](https://reference.aspose.com/diagram/java/com.aspose.diagram/event) class, geliştiricilerin ShapeSheet'te olay hücreleri ayarlamasına olanak tanır. Bu yardım konusu, geliştiricilerin olay hücrelerinde formülleri nasıl ayarlayabileceklerini gösterir:


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SettingEventCells.class);
// load diagram
Diagram diagram = new Diagram(dataDir + "TestTemplate.vsdm");
// get page
Page page = diagram.getPages().get(0);
// get shape id
long shapeId = page.addShape(3.0, 3.0, 0.36, 0.36, "Square");
// get shape
Shape shape = page.getShapes().getShape(shapeId);

// set event cells in the ShapeSheet
shape.getEvent().getEventXFMod().getUfe().setF("CALLTHIS(\"ThisDocument.ShowAlert\")");
shape.getEvent().getEventXFMod().getUfe().setF("CALLTHIS(\"ThisDocument.ShowAlert\")");
shape.getEvent().getEventXFMod().getUfe().setF("CALLTHIS(\"ThisDocument.ShowAlert\")");
shape.getEvent().getEventXFMod().getUfe().setF("CALLTHIS(\"ThisDocument.ShowAlert\")");
shape.getEvent().getEventXFMod().getUfe().setF("CALLTHIS(\"ThisDocument.ShowAlert\")");
shape.getEvent().getEventXFMod().getUfe().setF("CALLTHIS(\"ThisDocument.ShowAlert\")");

// save diagram
diagram.save(dataDir + "Output_NET.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}

