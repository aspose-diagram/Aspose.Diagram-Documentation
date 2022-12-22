---
title:  Visio'i PDF biçimine dönüştür
linktitle: Visio'i PDF'e dönüştür
type: docs
weight: 10
url: /tr/python-java/convert-visio-to-pdf/
description: This topic show you how to convert Visio to PDF formats using Aspose.Diagram for Python via Java. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM, VSSM to PDF with a few lines of code.
---
## **PDF'e aktarılıyor**
{{% alert color="primary" %}}

Python için Aspose.Diagram via Java API ve Sürüm Numarası ile ilgili bilgileri doğrudan çıktı belgelerine yazar. Örneğin, PDF'e bir Çizim oluşturulduğunda, Aspose.Diagram for Java doldurulur**Başvuru**'Aspose.Diagram' değerine sahip alan ve**PDF Yapımcı**değeri olan alan, örneğin 'Aspose.Diagram 17.9'.

Python via Java için Aspose.Diagram'e bu bilgileri çıktı Belgelerinden değiştirme veya kaldırma talimatı veremeyeceğinizi lütfen unutmayın.

{{% /alert %}}

Bu makalede, Python via Java için Aspose.Diagram kullanılarak bir Microsoft Visio diagram'in PDF'e nasıl aktarılacağı açıklanmaktadır.

diagram dosyalarını okumak için Diagram sınıfının yapıcısını ve diagram'i desteklenen herhangi bir görüntü formatına dışa aktarmak için Save yöntemini kullanın.

[VSD diagram](ExportToPDF.vsd)PDF'i dışa aktarmak için örnek çizim dosyasıdır. Diğer diagram formatlarını (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, 076137481 veya 40.1937610) kullanabilirsiniz.

VSD diagram'i PDF'e dışa aktarmak için:

1. Diagram sınıfının bir örneğini oluşturun.
1. Diagram sınıfı Save yöntemini çağırın ve çıktı formatını PDF olarak ayarlayın.

### **PDF Programlama Örneğine Aktarma**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToPDF.py" >}}

### **Birden Çok Sayfayı Böl**
Aspose.Diagram for Java, Microsoft Visio Diagram'i PDF'e dönüştürürken birden fazla sayfanın bölünmesine izin verir. Aşağıdaki kod parçacığı işlevselliği gösterir.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-VisioSaveOptions-UsePDFSaveOptions-SplitMultiPages.py" >}}
