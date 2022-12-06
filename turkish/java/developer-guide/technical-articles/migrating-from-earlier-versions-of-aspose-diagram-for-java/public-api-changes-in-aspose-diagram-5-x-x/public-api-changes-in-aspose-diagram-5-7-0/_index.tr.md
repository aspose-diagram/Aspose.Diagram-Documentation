---
title: Genel API Aspose.Diagram 5.7.0'daki değişiklikler
type: docs
weight: 30
url: /tr/java/public-api-changes-in-aspose-diagram-5-7-0/
---
{{% alert color="primary" %}} 

Bu belge, modül/uygulama geliştiricilerinin ilgisini çekebilecek 5.6.0 sürümünden 5.7.0 sürümüne Aspose.Diagram API değişikliklerini açıklamaktadır. Yalnızca yeni ve güncellenmiş genel yöntemleri değil, aynı zamanda Aspose.Diagram'deki perde arkasındaki davranışlardaki değişikliklerin açıklamasını da içerir.

{{% /alert %}} 
### **Zaman Çizelgesinde Tarih Modeli Dizilerini Ayarlama**
TimelineHelper sınıfına yeni setDateFormatStringForBE ve setDateFormatStringForIntm yöntemleri eklendi. Örnek kodlar:

**Java**

{{< highlight "java" >}}

 // set DateFormat String for start and finish of timeline shape

timelineHelper.setDateFormatStringForBE("yyyy-MM-dd");

// set DateFormat String for intm of timeline shape

timelineHelper.setDateFormatStringForIntm("yyyy-MM-dd");

{{< /highlight >}}
