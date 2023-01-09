---
title:  Visio'i PDF biçimine dönüştür
linktitle: Visio'i PDF'e dönüştür
type: docs
weight: 10
url: /tr/java/convert-visio-to-pdf/
description: Bu konu, Aspose.Diagram'in Visio'i PDF biçimlerine dönüştürmeye nasıl izin verdiğini gösterir. VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM'i birkaç satır kodla PDF'e dönüştürün.
---
## **PDF'e aktarılıyor**
{{% alert color="primary" %}}

Aspose.Diagram for Java, API ve Sürüm Numarası ile ilgili bilgileri doğrudan çıktı belgelerine yazar. Örneğin, PDF'e bir Çizim oluşturulduğunda, Aspose.Diagram for Java doldurulur**Başvuru**'Aspose.Diagram' değerine sahip alan ve**PDF Yapımcı**değeri olan alan, örneğin 'Aspose.Diagram 17.9'.

Lütfen Aspose.Diagram for Java API'e bu bilgileri çıktı Belgelerinden değiştirme veya kaldırma talimatı veremeyeceğinizi unutmayın.

{{% /alert %}}

 Bu makalede, bir Microsoft Visio diagram'in PDF kullanılarak nasıl dışa aktarılacağı açıklanmaktadır.[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 Kullan[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) diagram dosyalarını okumak için 'class' yapıcısı ve diagram'i desteklenen herhangi bir görüntü formatına dışa aktarmak için Save yöntemi.

The image below shows the VSD diagram that the code snippets below export PDF. You can use other diagram formats (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX or VSX) as well.

**Kaynak dosya.**

![yapılacaklar:resim_alternatif_Metin](how-to-convert-a-visio-diagram_1.png)

VSD diagram'i PDF'e dışa aktarmak için:

1. Diagram sınıfının bir örneğini oluşturun.
1. Diagram sınıfı Save yöntemini çağırın ve çıktı formatını PDF olarak ayarlayın.

Aşağıda PDF çıktı dosyasının bir görüntüsü bulunmaktadır.

**Çıktı PDF dosyası.**

![yapılacaklar:resim_alternatif_Metin](how-to-convert-a-visio-diagram_2.png)
### **PDF Programlama Örneğine Aktarma**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToPDF-ExportToPDF.java" >}}
### **Birden Çok Sayfayı Böl**
Aspose.Diagram for Java, Microsoft Visio Diagram'i PDF'e dönüştürürken birden fazla sayfanın bölünmesine izin verir. Aşağıdaki kod parçacığı işlevselliği gösterir.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UsePDFSaveOptions-SplitMultiPages.java" >}}
### **Sayfa Kaydetme Geri Aramasını Kullan**
Birden fazla sayfanız olması durumunda, Aspose.Diagram for Java, Microsoft Visio Diagram'i PDF'e dönüştürürken sayfa kaydetme geri aramasının kullanılmasına izin verir. Aşağıdaki kod parçacığı, işlevselliği gösterir.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-DiagramConversions-DocumentConversionProgress-1.java" >}}

#### **TestDiagramPageSavingCallback Sınıfı**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-DiagramConversions-DocumentConversionProgress-2.java" >}}
