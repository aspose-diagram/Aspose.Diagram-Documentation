---
title: Belge Dönüştürme İlerlemesini İzleme
type: docs
weight: 970
url: /tr/net/track-document-conversion-progress/
description: Bu bölümde, visio dosyalarının Aspose.Diagram ile dönüşüm ilerlemesinin nasıl izleneceği açıklanmaktadır.
---
## **Olası Kullanım Senaryoları**

 Bazen büyük visio dosyalarının dönüştürülmesi biraz zaman alabilir. Bu süre zarfında, uygulamanızın kullanılabilirliğini artırmak için yalnızca bir yükleme ekranı yerine belge dönüştürme ilerlemesini göstermek isteyebilirsiniz. Aspose.Diagram, aşağıdakileri sağlayarak izleme belgesi dönüştürme sürecini destekler:**[IPageSavingCallback](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback)** arayüz. bu**[IPageSavingCallback](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback)**arayüz sağlar**[PageStartSaving](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback/methods/pagestartsaving)**ve**[PageEndSaving](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback/methods/pageendsaving)**özel sınıfınızda uygulayabileceğiniz yöntemler. T'de gösterildiği gibi hangi sayfaların oluşturulacağını da kontrol edebilirsiniz.*estDiagramPageSavingCallback*özel sınıf

## **Belge Dönüştürme İlerlemesini İzleme**

 Aşağıdaki kod örneği,[kaynak visio dosyası](Drawing1.vsdx) kullanarak dönüştürme ilerlemesini konsolda yazdırır.*TestPageSavingCallback* uygulayan özel sınıf**[IPageSavingCallback](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback)**arayüz.

## **Basit kod**

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// create an instance PDF save options class
Aspose.Diagram.Saving.PdfSaveOptions options = new Aspose.Diagram.Saving.PdfSaveOptions();
          
//set page saving call back
options.PageSavingCallback = new TestDiagramPageSavingCallback();

// save Visio drawing
diagram.Save(dataDir + "Callback_out.pdf", options);

{{< /highlight >}}
```

için kod aşağıdadır*TestDiagramPageSavingCallback*özel sınıf

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
public class TestDiagramPageSavingCallback : Aspose.Diagram.Saving.IPageSavingCallback
{
    public void PageStartSaving(Aspose.Diagram.Saving.PageStartSavingArgs args)
    {
        Console.WriteLine("Start saving diagram page index {0} of pages {1}", args.PageIndex, args.PageCount);
    }

    public void PageEndSaving(Aspose.Diagram.Saving.PageEndSavingArgs args)
    {
        Console.WriteLine("End saving diagram page index {0} of pages {1}", args.PageIndex, args.PageCount);

        //don't output pages after page index 8.
        if (args.PageIndex >= 8)
        {
            args.HasMorePages = false;
        }
    }
}

{{< /highlight >}}
```

## **Konsol Çıkışı**

11. sayfaların 0. sayfa dizinini kaydetmeye başlayın</br>
11. sayfaların sayfa dizini 0'ı kaydetmeyi sonlandır</br>
11. sayfanın 1. sayfasını kaydetmeye başla</br>
11. sayfaların 1. sayfa indeksini kaydetmeyi sonlandır</br>
11. sayfanın 2. sayfasını kaydetmeye başla</br>
Kaydetmeyi sonlandır sayfa indeksi 2 sayfa 11</br>
Sayfa 11'in sayfa dizini 3'ü kaydetmeye başla</br>
Kaydetmeyi sonlandır sayfa indeksi 3 sayfa 11</br>
11. sayfanın 4. sayfasını kaydetmeye başla</br>
Kaydetmeyi sonlandır sayfa dizini 4 sayfa 11</br>
11. sayfanın 5. sayfasını kaydetmeye başla</br>
Kaydetmeyi sonlandır sayfa dizini 5 sayfa 11</br>
11. sayfanın 6. sayfasını kaydetmeye başla</br>
Kaydetmeyi sonlandır sayfa dizini 6 sayfa 11</br>
11. sayfanın 7. sayfasını kaydetmeye başla</br>
Kaydetmeyi sonlandır sayfa dizini 7 / sayfalar 11</br>
11. sayfanın 8. sayfasını kaydetmeye başla</br>
Kaydetmeyi sonlandır sayfa dizini 8 sayfa 11
