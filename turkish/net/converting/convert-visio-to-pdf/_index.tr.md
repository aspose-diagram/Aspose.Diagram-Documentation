---
title:  Visio'i PDF formatına dönüştür
linktitle: Visio'i PDF'ye dönüştür
type: docs
weight: 10
url: /tr/net/convert-visio-to-pdf/
description: Bu konuda, Aspose.Diagram'in Visio'i PDF biçimlerine dönüştürmeye nasıl izin verdiği gösterilmektedir. VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM'i birkaç satır kodla PDF'ye dönüştürün.
---
## **PDF'ye Aktar**
{{% alert color="primary" %}}

Aspose.Diagram for .NET, API ve Sürüm Numarası ile ilgili bilgileri doğrudan çıktı belgelerine yazar. Örneğin, bir Çizimi PDF olarak işledikten sonra Aspose.Diagram for .NET**Başvuru** 'Aspose.Diagram' değerine sahip alan ve**PDF Yapımcısı** değeri olan alan, örneğin 'Aspose.Diagram 17.9'.

Lütfen Aspose.Diagram for .NET API'e bu bilgileri çıktı Belgelerinden değiştirme veya kaldırma talimatı veremeyeceğinizi unutmayın.

{{% /alert %}}

 Bu makalede, bir Microsoft Visio diagram'in kullanılarak PDF'ye nasıl aktarılacağı açıklanmaktadır.[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API.

 Kullan[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) diagram dosyalarını okumak için sınıf yapıcısı ve diagram'i desteklenen herhangi bir görüntü formatına dışa aktarmak için Save yöntemi.

Aşağıdaki resim, aşağıdaki kod parçacıklarının PDF'yi dışa aktardığı VSD diagram'i göstermektedir. Diğer diagram formatlarını da (VSS, VSSM, VDX, VST, VSTX, VDX, VTX veya VSX) kullanabilirsiniz.

|**Kaynak dosya.**|
|:- |
|![yapılacaklar:resim_alternatif_Metin](how-to-convert-a-visio-diagram_1.png)|


VSD diagram'i PDF olarak dışa aktarmak için:

1. Diagram sınıfının bir örneğini oluşturun.
1. Diagram sınıfının Save yöntemini çağırın ve çıktı formatını PDF olarak ayarlayın.

Aşağıda çıktı PDF dosyasının bir görüntüsü bulunmaktadır.

|**Çıktı PDF dosyası.**|
|:- |
|![yapılacaklar:resim_alternatif_Metin](how-to-convert-a-visio-diagram_2.png)|
### **Microsoft Visio Çizimi PDF'e Aktar**
Kod örnekleri, Microsoft Visio Çiziminin C# kullanılarak PDF'ye nasıl aktarılacağını gösterir.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-ExportToPDF-ExportToPDF.cs" >}}
### **Birden Çok Sayfayı Böl**
Aspose.Diagram for .NET, Microsoft Visio Diagram'i PDF'ye dönüştürürken birden çok sayfanın bölünmesine izin verir. Aşağıdaki kod parçacığı işlevselliği gösterir.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UsePDFSaveOptions-SplitMultiPages.cs" >}}
### **Sayfa Kaydetme Geri Aramasını Kullan**
Birden fazla sayfanız olması durumunda, Aspose.Diagram for .NET, Microsoft Visio Diagram'i PDF'ye dönüştürürken sayfa kaydetme geri aramasının kullanılmasına izin verir. Aşağıdaki kod parçacığı işlevselliği gösterir.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UsePDFSaveOptions-PageSavingCallback.cs" >}}
#### **TestDiagramPageSavingCallback Sınıfı**
{{< highlight "java" >}}

 genel sınıf TestDiagramPageSavingCallback : Aspose.Diagram.Saving.IPageSavingCallback

{  genel geçersiz PageStartSaving(Aspose.Diagram.Saving.PageStartSavingArgs args)  {  Console.WriteLine("Sayfaların {1} diagram sayfasını {0} kaydetmeye başla", args.PageIndex + 1, args.x0000);  }  public void PageEndSaving(Aspose.Diagram.Saving.PageEndSavingArgs args)  {  Console.WriteLine("Sayfalardan {1} diagram sayfa {0} kaydetmeyi sonlandırın", args.PageIndex   //don't output pages after page index 8.  if (args.PageIndex >= 8)  {  args.HasMorePages = false;  }  }  }
