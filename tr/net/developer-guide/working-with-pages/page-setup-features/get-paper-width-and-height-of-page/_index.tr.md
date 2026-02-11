---
title: Sayfanın Kağıt Genişliğini ve Yüksekliğini Alın
type: docs
weight: 50
url: /tr/net/get-paper-width-and-height-of-page/
description: Bu bölümde visio sayfasının kağıt boyutunun Aspose.Diagram ile nasıl alınacağı açıklanmaktadır.
---
## **Olası Kullanım Senaryoları**

Bazen, sayfanın sayfa düzeninde ayarlandığı için kağıt boyutunun genişliğini ve yüksekliğini bilmeniz gerekir. lütfen[**PageProps.PageWidth**](https://reference.aspose.com/diagram/net/aspose.diagram/pageprops/properties/pagewidth)ve[**PageProps.PageHeight**](https://reference.aspose.com/diagram/net/aspose.diagram/pageprops/properties/pageheight)Bu amaç için özellikler.

## **Sayfa Genişliğini ve Sayfa Prop Yüksekliğini Alın**

 Aşağıdaki örnek kod, kullanımını açıklar[**PageProps.PageWidth**](https://reference.aspose.com/diagram/net/aspose.diagram/pageprops/properties/pagewidth)ve[**PageProps.PageHeight**](https://reference.aspose.com/diagram/net/aspose.diagram/pageprops/properties/pageheight)özellikleri.

### **Basit kod**


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Flow 1");

// Get page's width and height
double pagewidth = page.PageSheet.PageProps.PageWidth.Value;
double pageheight = page.PageSheet.PageProps.PageHeight.Value;

{{< /highlight >}}

