---
title: FitToSheetAcross'u Ayarlama
type: docs
weight: 10
url: /tr/net/setting-fittosheetacross/
description: Bu bölümde fittosheetacross'un Aspose.Diagram ile nasıl ayarlanacağı açıklanmaktadır.
---
{{% alert color="primary" %}}

Bazen, sayfaların yazdırmayı kontrol etmesi için sayfa kurulum ayarlarını yapılandırmak gerekir. Bu sayfa yapısı ayarları çeşitli seçenekler sunar.

{{% /alert %}}

## **FitToSheetAcross'u Ayarlama**

Sayfa yapısı seçenekleri Aspose.Diagram'de tam olarak desteklenir. Bu makale, Aspose.Diagram ile sayfa seçeneklerinin nasıl ayarlanacağını açıklar ve ayar için kod örneklerini gösterir:

 Aspose.Diagram bir sınıf sağlar,[**Sayfa**](https://reference.aspose.com/diagram/net/aspose.diagram/page) , bu bir Microsoft Visio dosyasını temsil eder. bu[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/page) sınıf bir içerir[**Sayfalar**](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection) Visio dosyasındaki her sayfaya erişim sağlayan koleksiyon. Bir sayfa şununla temsil edilir:[**Sayfa**](https://reference.aspose.com/diagram/net/aspose.diagram/page)sınıf.

 bu[**Sayfa Sayfası**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) sınıf sağlar[**Baskı Destekleri**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) sayfanın sayfa düzeni seçeneklerini ayarlamak için kullanılan özellik. Aslında, bu[**Baskı Destekleri**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) özellik bir nesnedir[**Sayfa Sayfası**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) yazdırılan bir sayfa için farklı sayfa düzeni seçeneklerini ayarlamak için kullanılan sınıf. bu[**Baskı Destekleri**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops)class, sayfa düzeni seçeneklerini ayarlamak için kullanılan çeşitli özellikler sağlar. Bu özelliklerden bazıları aşağıda tartışılmaktadır.

### **Sayfa Boyunca Sığdır**


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Print();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

PrintProps printProps = diagram.Pages[0].PageSheet.PrintProps;

printProps.OnPage.Value = BOOL.True;

//Set Fit to sheet(s) across
printProps.PagesX.Value = 1;

//Set By sheet(s) down
printProps.PagesY.Value = 1;

{{< /highlight >}}



