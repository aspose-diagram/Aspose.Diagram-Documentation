---
title: Yazdırma Seçeneklerini Ayarlama
type: docs
weight: 10
url: /tr/net/setting-print-options/
description: Bu bölümde, Aspose.Diagram ile yazdırma seçeneklerinin nasıl ayarlanacağı açıklanmaktadır.
---
{{% alert color="primary" %}}

Bazen, sayfaların yazdırmayı kontrol etmesi için sayfa kurulum ayarlarını yapılandırmak gerekir. Bu sayfa yapısı ayarları çeşitli seçenekler sunar.

{{% /alert %}}

## **Yazdırma Seçeneklerini Ayarlama**

Sayfa yapısı seçenekleri Aspose.Diagram'de tam olarak desteklenir. Bu makale, Aspose.Diagram ile sayfa seçeneklerinin nasıl ayarlanacağını açıklar ve ayar için kod örneklerini gösterir:

 Aspose.Diagram bir sınıf sağlar,[**Sayfa**](https://reference.aspose.com/diagram/net/aspose.diagram/page) , bu bir Microsoft Visio dosyasını temsil eder. bu[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/page) sınıf bir içerir[**Sayfalar**](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection) Visio dosyasındaki her sayfaya erişim sağlayan koleksiyon. Bir sayfa şununla temsil edilir:[**Sayfa**](https://reference.aspose.com/diagram/net/aspose.diagram/page)sınıf.

 bu[**Sayfa Sayfası**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) sınıf sağlar[**Baskı Destekleri**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) sayfanın sayfa düzeni seçeneklerini ayarlamak için kullanılan özellik. Aslında, bu[**Baskı Destekleri**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) özellik bir nesnedir[**Sayfa Sayfası**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) yazdırılan bir sayfa için farklı sayfa düzeni seçeneklerini ayarlamak için kullanılan sınıf. bu[**Baskı Destekleri**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops)class, sayfa düzeni seçeneklerini ayarlamak için kullanılan çeşitli özellikler sağlar. Bu özelliklerden bazıları aşağıda tartışılmaktadır.

### **Sayfa Yönünü Yazdır**

 Yazdır Sayfa yönü, dikey veya yatay olarak ayarlanabilir.[**Baskı Destekleri**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) sınıf'[**Sayfa Yönünü Yazdır**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/printpageorientation) Emlak. bu[**Sayfa Yönünü Yazdır**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/printpageorientation) özelliği, önceden tanımlanmış değerlerden birini kabul eder.[**PrintPageOrientationValue**](https://reference.aspose.com/diagram/net/aspose.diagram/printpageorientationvalue)numaralandırma, aşağıda listelenmiştir.

|**Sayfa Yönü Tiplerini Yazdır**|**Tanım**|
|:- |:- |
|AynıYazıcıyla Aynı|Yazıcı yönüyle aynı|
|Manzara|Yatay yönlendirme|
|Vesika|Dikey yönlendirme|

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Print();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

//Get page
Aspose.Diagram.Page page = diagram.Pages.GetPage(0);

//Set PrintPageOrientation
page.PageSheet.PrintProps.PrintPageOrientation.Value = PrintPageOrientationValue.Landscape;

{{< /highlight >}}
```

### **Ölçekleme faktörü**

 Ölçekleme faktörünü ayarlayarak bir sayfanın boyutunu küçültmek veya büyütmek mümkündür.[**ÖlçekX**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/scalex)Emlak.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Print();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

//Set ScaleX and ScaleY
diagram.Pages[0].PageSheet.PrintProps.ScaleX.Value = 1;
diagram.Pages[0].PageSheet.PrintProps.ScaleY.Value = 1;

{{< /highlight >}}
```
