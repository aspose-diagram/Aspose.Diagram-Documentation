---
title:  Visio'i HTML biçimine dönüştür
linktitle: Visio'i HTML'ye dönüştür
type: docs
weight: 30
url: /tr/net/convert-visio-to-html/
description: Bu konu, Aspose.Diagram'in Visio'i html biçimlerine dönüştürmeye nasıl izin verdiğini gösterir. VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM'i birkaç satır kodla html'ye dönüştürün.
---
## **Visio'i HTML'ye aktar**
 Bu makalede, bir Microsoft Visio diagram'in kullanılarak HTML'ye nasıl aktarılacağı açıklanmaktadır.[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API.

 Kullan[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) diagram dosyalarını okumak için sınıf yapıcısı ve diagram'i desteklenen herhangi bir görüntü formatına dışa aktarmak için Save yöntemi. Geliştiriciler, ortaya çıkan HTML'yi yerel depolamaya veya doğrudan bir akış örneğine kaydedebilir.

1. [Ortaya çıkan HTML'yi yerel depolamaya kaydedin](https://docs.aspose.com/diagram/net/convert-visio-to-html/#save-resultant-html-in-the-local-storage).
1. [Elde edilen HTML'yi bir akış örneğine kaydedin](https://docs.aspose.com/diagram/net/convert-visio-to-html/#save-resultant-html-in-a-stream-instance).

Aşağıdaki resimde, PNG formatında kaydedilmek üzere olan bir VSD dosyası gösterilmektedir. Diğer diagram formatlarını da (VSDX, VSDM, VSTX, VSSX, VSS, VSSM, VDX, VST, VSTX, VDX, VTX1 veya 3.761) kullanabilirsiniz.

|**diagram'i girin.**|
|:- |
|![yapılacaklar:resim_alternatif_Metin](how-to-convert-a-visio-diagram_6.png)|
VSD diagram'i HTML'ye aktarmak için aşağıdaki adımları gerçekleştirin:

1. Diagram sınıfının bir örneğini oluşturun.
1. Dagram sınıfının Save yöntemini çağırın ve çıktı formatı olarak HTML'yi ayarlayın.
### **Ortaya çıkan HTML'yi yerel depolamaya kaydedin**
Ortaya çıkan dosya, dosya adı ve uzantısı dahil olmak üzere tam bir yol dizesi iletilerek kaydedilebilir, örneğin @"c:\temp\MyOutput.html".
#### **Sonuç HTML'sini Yerel Depolama Programlama Örneğine Kaydet**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-ExportToHTML-ExportToHTML.cs" >}}



### **Elde edilen HTML'yi bir akış örneğine kaydedin**
Ortaya çıkan HTML'yi yerel depoda saklamadan bir veritabanına veya havuza kaydetmek kullanım durumu içindir. Bu özellik aynı zamanda HTML'nin diğer sonuç kaynaklarını, örneğin yazı tiplerini, CSS'yi (stil bilgilerini içeren) ve resimleri de gömer. Akış örneğine tek bir HTML dosyası kaydettiği için.
#### **Sonuç HTML'sini Akış Programlama Örneğine Kaydetme**
{{< highlight "java" >}}

 // Load an existing visio diagram

Diagram diagram = new Diagram("Basic Flowchart.vsd");

// Save resultant HTML directly to a stream

MemoryStream stream = new MemoryStream();

diagram.Save(stream, SaveFileFormat.HTML);



{{< /highlight >}}
