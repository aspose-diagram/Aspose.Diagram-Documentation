---
title:  Visio'i HTML biçimine dönüştür
linktitle: Visio'i HTML'e dönüştür
type: docs
weight: 30
url: /tr/net/convert-visio-to-html/
description: Bu konu, Aspose.Diagram'in Visio'i html biçimlerine dönüştürmeye nasıl izin verdiğini gösterir. VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM'i birkaç satır kodla html'ye dönüştürün.
---
## **Visio'i HTML'e aktar**
 Bu makalede, bir Microsoft Visio diagram'in HTML kullanılarak nasıl dışa aktarılacağı açıklanmaktadır.[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API.

 Kullan[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) diagram dosyalarını okumak için sınıf yapıcısı ve diagram'i desteklenen herhangi bir görüntü formatına dışa aktarmak için Save yöntemi. Geliştiriciler, ortaya çıkan HTML'i yerel depolamaya veya doğrudan bir akış örneğine kaydedebilir.

1. [Ortaya çıkan HTML'i yerel depoya kaydedin](https://docs.aspose.com/diagram/net/convert-visio-to-html/#save-resultant-html-in-the-local-storage).
1. [Elde edilen HTML'i bir akış örneğine kaydedin](https://docs.aspose.com/diagram/net/convert-visio-to-html/#save-resultant-html-in-a-stream-instance).

Aşağıdaki resimde, PNG biçiminde kaydedilmek üzere olan bir VSD dosyası gösterilmektedir. Diğer diagram formatlarını da kullanabilirsiniz (VSDX, VSDM, VSTX, VSSX, VSS, VSSM, VDX, VST, VSTX, VDX, 04811203)

|**diagram'i girin.**|
|:- |
|![yapılacaklar:resim_alternatif_Metin](how-to-convert-a-visio-diagram_6.png)|
VSD diagram'i HTML'e aktarmak için aşağıdaki adımları gerçekleştirin:

1. Diagram sınıfının bir örneğini oluşturun.
1. Dagram sınıfının Save yöntemini çağırın ve çıktı formatı olarak HTML'i ayarlayın.
### **Ortaya çıkan HTML'i yerel depoya kaydedin**
Ortaya çıkan dosya, dosya adı ve uzantısı dahil olmak üzere tam bir yol dizesi iletilerek kaydedilebilir, örneğin @"c:\temp\MyOutput.html".
#### **Sonuç HTML'i Yerel Depolama Programlama Örneğine Kaydet**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();
// Load diagram
Diagram diagram = new Diagram(dataDir + "ExportToHTML.vsd");
// Save diagram
diagram.Save(dataDir + "outputVSDtoHTML.html", SaveFileFormat.HTML);

{{< /highlight >}}
```



### **Elde edilen HTML'i bir akış örneğine kaydedin**
Elde edilen HTML'i yerel depoda saklamadan bir veritabanına veya havuza kaydetmek kullanım durumu içindir. Bu özellik aynı zamanda HTML'in diğer sonuç kaynaklarını, örneğin yazı tiplerini, CSS'yi (stil bilgilerini içeren) ve resimleri de içerir. Akış örneğine tek bir HTML dosyası kaydettiği için.
#### **Sonuç HTML'i Akış Programlama Örneğine Kaydet**
{{< highlight "java" >}}

 // Load an existing visio diagram

Diagram diagram = new Diagram("Basic Flowchart.vsd");

// Save resultant HTML directly to a stream

MemoryStream stream = new MemoryStream();

diagram.Save(stream, SaveFileFormat.HTML);



{{< /highlight >}}
