---
title:  Visio'i PDF biçimine dönüştür
linktitle: Visio'i PDF'e dönüştür
type: docs
weight: 10
url: /tr/net/convert-visio-to-pdf/
description: Bu konu, Aspose.Diagram'in Visio'i PDF biçimlerine dönüştürmeye nasıl izin verdiğini gösterir. VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM'i birkaç satır kodla PDF'e dönüştürün.
---
## **PDF'e aktar**
{{% alert color="primary" %}}

Aspose.Diagram for .NET, API ve Sürüm Numarası ile ilgili bilgileri doğrudan çıktı belgelerine yazar. Örneğin, PDF'e bir Çizim oluşturulduğunda, Aspose.Diagram for .NET doldurulur**Başvuru** 'Aspose.Diagram' değerine sahip alan ve**PDF Yapımcı** değeri olan alan, örneğin 'Aspose.Diagram 17.9'.

Lütfen Aspose.Diagram for .NET API'e bu bilgileri çıktı Belgelerinden değiştirme veya kaldırma talimatı veremeyeceğinizi unutmayın.

{{% /alert %}}

 Bu makalede, bir Microsoft Visio diagram'in PDF kullanılarak nasıl dışa aktarılacağı açıklanmaktadır.[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API.

 Kullan[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) diagram dosyalarını okumak için sınıf yapıcısı ve diagram'i desteklenen herhangi bir görüntü formatına dışa aktarmak için Save yöntemi.

Aşağıdaki resim VSD diagram'i gösteriyor ki aşağıdaki kod parçacıkları PDF'i dışa aktarıyor. Diğer diagram formatlarını da kullanabilirsiniz (VSS, VSSM, VDX, VST, VSTX, 076183034, 0761 veya 3761 veya 376193)

|**Kaynak dosya.**|
|:- |
|![yapılacaklar:resim_alternatif_Metin](how-to-convert-a-visio-diagram_1.png)|


VSD diagram'i PDF'e dışa aktarmak için:

1. Diagram sınıfının bir örneğini oluşturun.
1. Diagram sınıfı Save yöntemini çağırın ve çıktı formatını PDF olarak ayarlayın.

Aşağıda PDF çıktı dosyasının bir görüntüsü bulunmaktadır.

|**Çıktı PDF dosyası.**|
|:- |
|![yapılacaklar:resim_alternatif_Metin](how-to-convert-a-visio-diagram_2.png)|
### **İhracat Microsoft Visio Çizimi PDF'e**
Kod örnekleri, Microsoft Visio Çiziminin C# kullanılarak PDF'e nasıl aktarılacağını gösterir.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-ExportToPDF-ExportToPDF.cs" >}}
### **Birden Çok Sayfayı Böl**
Aspose.Diagram for .NET, Microsoft Visio Diagram'i PDF'e dönüştürürken birden fazla sayfanın bölünmesine izin verir. Aşağıdaki kod parçacığı işlevselliği gösterir.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UsePDFSaveOptions-SplitMultiPages.cs" >}}
### **Sayfa Kaydetme Geri Aramasını Kullan**
Birden fazla sayfanız olması durumunda, Aspose.Diagram for .NET, Microsoft Visio Diagram'i PDF'e dönüştürürken sayfa kaydetme geri aramasının kullanılmasına izin verir. Aşağıdaki kod parçacığı, işlevselliği gösterir.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UsePDFSaveOptions-PageSavingCallback.cs" >}}
#### **TestDiagramPageSavingCallback Sınıfı**
{{< highlight "java" >}}

 genel sınıf TestDiagramPageSavingCallback : Aspose.Diagram.Saving.IPageSavingCallback

{  genel geçersiz PageStartSaving(Aspose.Diagram.Saving.PageStartSavingArgs args)  {  Console.WriteLine("Sayfaların {1} diagram sayfasını {0} kaydetmeye başla", args.PageIndex + 1, args.x0000);  }  public void PageEndSaving(Aspose.Diagram.Saving.PageEndSavingArgs args)  {  Console.WriteLine("Sayfalardan {1} diagram sayfa {0} kaydetmeyi sonlandırın", args.PageIndex   //don't output pages after page index 8.  if (args.PageIndex >= 8)  {  args.HasMorePages = false;  }  }  }
