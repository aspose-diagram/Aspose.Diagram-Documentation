---
title:  Visio'i HTML biçimine dönüştür
linktitle: Visio'i HTML'e dönüştür
type: docs
weight: 30
url: /tr/java/convert-visio-to-html/
description: Bu konu, Aspose.Diagram'in Visio'i html biçimlerine dönüştürmeye nasıl izin verdiğini gösterir. VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM'i birkaç satır kodla html'ye dönüştürün.
---
## **Visio'i HTML'e aktar** **Visio'i HTML'e aktar**
 Bu makalede, bir Microsoft Visio diagram'in HTML kullanılarak nasıl dışa aktarılacağı açıklanmaktadır.[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 Kullan[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) diagram dosyalarını okumak için sınıf yapıcısı ve diagram'i desteklenen herhangi bir görüntü formatına dışa aktarmak için Save yöntemi. Geliştiriciler, ortaya çıkan HTML'i yerel depolamaya veya doğrudan bir akış örneğine kaydedebilir.

1. [Ortaya çıkan HTML'i yerel depoya kaydedin](/diagram/tr/java/how-to-convert-a-visio-diagram/).
1. [Elde edilen HTML'i bir akış örneğine kaydedin](/diagram/tr/java/how-to-convert-a-visio-diagram/).

Aşağıdaki resimde, PNG biçiminde kaydedilmek üzere olan bir VSD dosyası gösterilmektedir. Diğer diagram formatlarını da kullanabilirsiniz (VSDX, VSTM, VSTM, VSSX, VSS, VSSM, VDX, VST, VSTX, VDX, 04811203)

**diagram'i girin.**

![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/YX4BNNq.png)

VSD diagram'i HTML'e aktarmak için aşağıdaki adımları gerçekleştirin:

1. Diagram sınıfının bir örneğini oluşturun.
1. Dagram sınıfının Save yöntemini çağırın ve çıktı formatı olarak HTML'i ayarlayın.

Aşağıdaki görüntü HTML çıktı dosyasını göstermektedir.

**Çıkış HTML diagram.**

![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/syavUqI.png)
### **Ortaya çıkan HTML'i yerel depoya kaydedin**
Ortaya çıkan dosya, dosya adı ve uzantısı dahil olmak üzere tam bir yol dizesi iletilerek kaydedilebilir, örneğin @"c:\temp\MyOutput.html".
#### **Sonuç HTML'i Yerel Depolama Programlama Örneğine Kaydet**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExportToHTML.class);

// call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "ExportToHTML.vsd");

// Save as HTML
diagram.save(dataDir + "ExportToHTML_Out.html", SaveFileFormat.HTML);

{{< /highlight >}}
```



### **Elde edilen HTML'i bir akış örneğine kaydedin**
Elde edilen HTML'i yerel depoda saklamadan bir veritabanına veya havuza kaydetmek kullanım durumu içindir. Bu özellik aynı zamanda HTML'in diğer sonuç kaynaklarını, örneğin yazı tiplerini, CSS'yi (stil bilgilerini içeren) ve resimleri de içerir. Akış örneğine tek bir HTML dosyası kaydettiği için.
#### **Sonuç HTML'i Akış Programlama Örneğine Kaydet**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExportHTMLinStream.class);
// load diagram
Diagram diagram = new Diagram(dataDir + "ExportToHTML.vsd");
// save resultant HTML directly to a stream
ByteArrayOutputStream dstStream = new ByteArrayOutputStream();
diagram.save(dstStream, SaveFileFormat.HTML);
// In you want to read the result into a Diagram object again, in Java you need to get the
// data bytes and wrap into an input stream.
ByteArrayInputStream srcStream = new ByteArrayInputStream(dstStream.toByteArray());

{{< /highlight >}}
```
