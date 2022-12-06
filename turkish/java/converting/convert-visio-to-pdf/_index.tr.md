---
title:  Visio'i PDF formatına dönüştür
linktitle: Visio'i PDF'ye dönüştür
type: docs
weight: 10
url: /tr/java/convert-visio-to-pdf/
description: Bu konuda, Aspose.Diagram'in Visio'i PDF biçimlerine dönüştürmeye nasıl izin verdiği gösterilmektedir. VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM'i birkaç satır kodla PDF'ye dönüştürün.
---
## **PDF'ye dışa aktarma**
{{% alert color="primary" %}}

Aspose.Diagram for Java, API ve Sürüm Numarası ile ilgili bilgileri doğrudan çıktı belgelerine yazar. Örneğin, bir Çizimi PDF olarak işledikten sonra Aspose.Diagram for Java**Başvuru**'Aspose.Diagram' değerine sahip alan ve**PDF Yapımcısı**değeri olan alan, örneğin 'Aspose.Diagram 17.9'.

Lütfen Aspose.Diagram for Java API'e bu bilgileri çıktı Belgelerinden değiştirme veya kaldırma talimatı veremeyeceğinizi unutmayın.

{{% /alert %}}

 Bu makalede, bir Microsoft Visio diagram'in kullanılarak PDF'ye nasıl aktarılacağı açıklanmaktadır.[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 Kullan[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) diagram dosyalarını okumak için 'class' yapıcısı ve diagram'i desteklenen herhangi bir görüntü formatına dışa aktarmak için Save yöntemi.

Aşağıdaki resim, aşağıdaki kod parçacıklarının PDF'yi dışa aktardığı VSD diagram'i göstermektedir. Diğer diagram formatlarını da (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX veya VSX) kullanabilirsiniz.

**Kaynak dosya.**

![yapılacaklar:resim_alternatif_Metin](how-to-convert-a-visio-diagram_1.png)

VSD diagram'i PDF olarak dışa aktarmak için:

1. Diagram sınıfının bir örneğini oluşturun.
1. Diagram sınıfının Save yöntemini çağırın ve çıktı formatını PDF olarak ayarlayın.

Aşağıda çıktı PDF dosyasının bir görüntüsü bulunmaktadır.

**Çıktı PDF dosyası.**

![yapılacaklar:resim_alternatif_Metin](how-to-convert-a-visio-diagram_2.png)
### **PDF Programlama Örneğine Aktarma**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToPDF-ExportToPDF.java" >}}
### **Birden Çok Sayfayı Böl**
Aspose.Diagram for Java, Microsoft Visio Diagram'i PDF'ye dönüştürürken birden çok sayfanın bölünmesine izin verir. Aşağıdaki kod parçacığı işlevselliği gösterir.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UsePDFSaveOptions-SplitMultiPages.java" >}}
### **Sayfa Kaydetme Geri Aramasını Kullan**
Birden fazla sayfanız olması durumunda, Aspose.Diagram for Java, Microsoft Visio Diagram'i PDF'ye dönüştürürken sayfa kaydetme geri aramasının kullanılmasına izin verir. Aşağıdaki kod parçacığı işlevselliği gösterir.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-DiagramConversions-DocumentConversionProgress-1.java" >}}

#### **TestDiagramPageSavingCallback Sınıfı**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-DiagramConversions-DocumentConversionProgress-2.java" >}}
