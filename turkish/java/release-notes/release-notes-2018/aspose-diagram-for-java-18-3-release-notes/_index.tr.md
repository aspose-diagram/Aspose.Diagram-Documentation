---
title: Aspose.Diagram for Java 18.3 Sürüm Notları
type: docs
weight: 100
url: /tr/java/aspose-diagram-for-java-18-3-release-notes/
---
{{% alert color="primary" %}} 

 Bu sayfa için sürüm notları içerir[Aspose.Diagram for Java 18.3](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-18-3-release-notes/).

{{% /alert %}} 
## **İyileştirmeler ve Değişiklikler**

|**Anahtar**|**Özet**|**Kategori**|
|:- |:- |:- |
|DIAGRAMJAVA-50592|NewValue işleme yönergeleri için destek ekleyin|Artırma|
|DIAGRAMJAVA-50150|Şekil TabsCollection nesnelerine erişilemiyor|Böcek|
|DIAGRAMJAVA-50588|Çıktı VSDX - büyük boyutlu bir şekil eklendi|Böcek|
|DIAGRAMJAVA-50593|VSDX'den SVG'ye - yanlış metin ve arka plan renkleri|Böcek|
|DIAGRAMJAVA-50595|Diagram, VSDX belgesini kaydederken siyah beyaza dönüyor|Böcek|
### **Page sınıfına moveTo üyesi ekler**
moveTo üyesi, Visio çiziminde sayfanın konumunu taşımak için hedef sayfa dizinini parametre olarak alır.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page(1);

// move page in the diagram

newPage.moveTo(2);

diagram.save(dataDir + "Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **Kullanım Örnekleri**
Lütfen Aspose.Diagram Wiki belgelerine eklenen yardım konularının listesini kontrol edin:

1. [Visio çiziminde Sayfa konumunu taşı]
