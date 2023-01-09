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

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Event-Section-SettingCellsInEventSection-SettingCellsInEventSection.cs" >}}
