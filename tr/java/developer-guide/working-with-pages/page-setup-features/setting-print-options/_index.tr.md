---
title: Yazdırma Seçeneklerini Ayarlama
type: docs
weight: 10
url: /tr/java/setting-print-options/
description: Bu bölümde, Aspose.Diagram ile yazdırma seçeneklerinin nasıl ayarlanacağı açıklanmaktadır.
---
{{% alert color="primary" %}}

Bazen, sayfaların yazdırmayı kontrol etmesi için sayfa kurulum ayarlarını yapılandırmak gerekir. Bu sayfa yapısı ayarları çeşitli seçenekler sunar.

{{% /alert %}}

## **Yazdırma Seçeneklerini Ayarlama**

Sayfa yapısı seçenekleri Aspose.Diagram'de tam olarak desteklenir. Bu makale, Aspose.Diagram ile sayfa seçeneklerinin nasıl ayarlanacağını açıklar ve ayar için kod örneklerini gösterir:

 Aspose.Diagram bir sınıf sağlar,[**Sayfa**](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) , bu bir Microsoft Visio dosyasını temsil eder. bu[**Diagram**](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) sınıf bir içerir[**Sayfalar**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagecollection) Visio dosyasındaki her sayfaya erişim sağlayan koleksiyon. Bir sayfa şununla temsil edilir:[**Sayfa**](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)sınıf.

 bu[**Sayfa Sayfası**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet) sınıf sağlar[**Baskı Destekleri**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps) sayfanın sayfa düzeni seçeneklerini ayarlamak için kullanılan özellik. Aslında, bu[**Baskı Destekleri**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps) özellik bir nesnedir[**Sayfa Sayfası**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet) yazdırılan bir sayfa için farklı sayfa düzeni seçeneklerini ayarlamak için kullanılan sınıf. bu[**Baskı Destekleri**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps)class, sayfa düzeni seçeneklerini ayarlamak için kullanılan çeşitli özellikler sağlar. Bu özelliklerden bazıları aşağıda tartışılmaktadır.

### **Sayfa Yönünü Yazdır**

 Yazdır Sayfa yönü, dikey veya yatay olarak ayarlanabilir.[**Baskı Destekleri**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps) sınıf'[**Sayfa Yönünü Yazdır**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#PrintPageOrientation) Emlak. bu[**Sayfa Yönünü Yazdır**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#PrintPageOrientation) özelliği, önceden tanımlanmış değerlerden birini kabul eder.[**PrintPageOrientationValue**](https://reference.aspose.com/diagram/java/com.aspose.diagram/PrintPageOrientationValue)numaralandırma, aşağıda listelenmiştir.

|**Sayfa Yönü Tiplerini Yazdır**|**Tanım**|
|:- |:- |
|AynıYazıcıyla Aynı|Yazıcı yönüyle aynı|
|Manzara|Yatay yönlendirme|
|Vesika|Dikey yönlendirme|

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Print-SetPageOrientation-SetPageOrientation.java" >}}

### **Ölçekleme faktörü**

 Ölçekleme faktörünü ayarlayarak bir sayfanın boyutunu küçültmek veya büyütmek mümkündür.[**ÖlçekX**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#ScaleX)Emlak.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Print-SetPageOrientation-SetPageScale.java" >}}
