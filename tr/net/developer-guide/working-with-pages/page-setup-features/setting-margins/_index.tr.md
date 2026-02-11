---
title: Kenar Boşluklarını Ayarlama
type: docs
weight: 20
url: /tr/net/setting-margins/
description: Bu bölümde visio'in sayfa seçeneklerinin Aspose.Diagram ile nasıl ayarlanacağı açıklanmaktadır.
---
{{% alert color="primary" %}}

Aspose.Diagram, Microsoft Visio'in sayfa düzeni seçeneklerini tam olarak destekler. Geliştiricilerin, yazdırma sürecini kontrol etmek için sayfalar için sayfa kurulum ayarlarını yapılandırması gerekebilir. Bu konuda, sayfa kenar boşluklarını yapılandırmak için Aspose.Diagram'in nasıl kullanılacağı anlatılmaktadır.

{{% /alert %}}

## **Kenar Boşluklarını Ayarlama**

 Aspose.Diagram bir sınıf sağlar,[**Sayfa**](https://reference.aspose.com/diagram/net/aspose.diagram/page) , bu bir Microsoft Visio dosyasını temsil eder. bu[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/page) sınıf bir içerir[**Sayfalar**](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection) Visio dosyasındaki her sayfaya erişim sağlayan koleksiyon. Bir sayfa şununla temsil edilir:[**Sayfa**](https://reference.aspose.com/diagram/net/aspose.diagram/page)sınıf.

 bu[**Sayfa Sayfası**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) sınıf sağlar[**Baskı Destekleri**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) sayfanın sayfa düzeni seçeneklerini ayarlamak için kullanılan özellik. Aslında, bu[**Baskı Destekleri**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) özellik bir nesnedir[**Sayfa Sayfası**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) yazdırılan bir sayfa için farklı sayfa düzeni seçeneklerini ayarlamak için kullanılan sınıf. bu[**Baskı Destekleri**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops)class, sayfa düzeni seçeneklerini ayarlamak için kullanılan çeşitli özellikler sağlar. Bu özelliklerden bazıları aşağıda tartışılmaktadır.

### **Sayfa Kenar Boşlukları**

 kullanarak sayfa kenar boşluklarını ayarlayın (PageTopMargin, PageBottomMargin, PageLeftMargin, PageRightMargin)[**Baskı Destekleri**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops)sınıf üyeleri. Sayfa kenar boşluklarını belirtmek için kullanılan yöntemlerden birkaçı aşağıda listelenmiştir:

- [**PageTopMargin**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/pagetopmargin)
- [**PageBottomMargin**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/pagebottommargin)
- [**SayfaSolMarj**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/pageleftmargin)
- [**SayfaSağMargin**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/pagerightmargin)

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Print();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

//Set Page Margin
diagram.Pages[0].PageSheet.PrintProps.PageLeftMargin.Value = 0.01;
diagram.Pages[0].PageSheet.PrintProps.PageRightMargin.Value = 0.01;
diagram.Pages[0].PageSheet.PrintProps.PageTopMargin.Value = 0.01;
diagram.Pages[0].PageSheet.PrintProps.PageBottomMargin.Value = 0.01;
{{< /highlight >}}
```