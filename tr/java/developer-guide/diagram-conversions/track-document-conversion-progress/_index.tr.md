---
title: Belge Dönüştürme İlerlemesini İzleme
type: docs
weight: 970
url: /tr/java/track-document-conversion-progress/
description: Bu bölümde, visio dosyalarının Aspose.Diagram ile dönüşüm ilerlemesinin nasıl izleneceği açıklanmaktadır.
---
## **Olası Kullanım Senaryoları**

Bazen büyük visio dosyalarının dönüştürülmesi biraz zaman alabilir. Bu süre zarfında, uygulamanızın kullanılabilirliğini artırmak için yalnızca bir yükleme ekranı yerine belge dönüştürme ilerlemesini göstermek isteyebilirsiniz. Aspose.Diagram, IPageSavingCallback arabirimini sağlayarak belge dönüştürme sürecini izlemeyi destekler. IPageSavingCallback arabirimi, özel sınıfınızda uygulayabileceğiniz PageStartSaving ve PageEndSaving yöntemleri sağlar. T'de gösterildiği gibi hangi sayfaların oluşturulacağını da kontrol edebilirsiniz.*estDiagramPageSavingCallback*özel sınıf

## **Belge Dönüştürme İlerlemesini İzleme**

 Aşağıdaki kod örneği,[kaynak visio dosyası](Drawing1.vsdx) kullanarak dönüştürme ilerlemesini konsolda yazdırır.*TestPageSavingCallback*IPageSavingCallback arabirimini uygulayan özel sınıf.

## **Basit kod**

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(DetectFormatfromInputStream.class);

// Open the stream. Read only access to load a Visio diagram.
String stream = new String(dataDir + "Drawing1.vsdx");
// detect file format using an input stream
FileFormatInfo info = FileFormatUtil.detectFileFormat(stream);

// get the detected file format
System.out.println("The spreadsheet format is: " + info.getFileFormatType());

{{< /highlight >}}
```

için kod aşağıdadır*TestDiagramPageSavingCallback*özel sınıf

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(DetectFormatfromInputStream.class);

// Open the stream. Read only access to load a Visio diagram.
String stream = new String(dataDir + "Drawing1.vsdx");
// detect file format using an input stream
FileFormatInfo info = FileFormatUtil.detectFileFormat(stream);

// get the detected file format
System.out.println("The spreadsheet format is: " + info.getFileFormatType());

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
