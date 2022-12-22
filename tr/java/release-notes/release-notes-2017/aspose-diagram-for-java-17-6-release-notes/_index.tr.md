---
title: Aspose.Diagram for Java 17.6 Sürüm Notları
type: docs
weight: 70
url: /tr/java/aspose-diagram-for-java-17-6-release-notes/
---
{{% alert color="primary" %}} 

 Bu sayfa için sürüm notları içerir[Aspose.Diagram for Java 17.6](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-17-6-release-notes/).

{{% /alert %}} 
## **İyileştirmeler ve Değişiklikler**

|**Anahtar**|**Özet**|**Kategori**|
|:- |:- |:- |
|DIAGRAMJAVA-50500|Çıktı VSDX - manuel olarak eklenen şekil boyutu değiştirilmiyor|Artırma|
|DIAGRAMJAVA-50503|Çıktı VSDX - çok satırlı metin eklerken metin taşması|Artırma|
|DIAGRAMJAVA-50505|Çizim sayfası resme dönüştürülürken boş işaretçi hatası oluştu|Böcek|
|DIAGRAMJAVA-50484|Bir çizimi VSDX formatında kaydederken karar kutusu şeklinin dikey metin gösterimi|Böcek|
|DIAGRAMJAVA-50486|Bir çizimi VSDX formatında kaydederken Önceden tanımlanmış işlem şeklinin dikey metin görüntüsü|Böcek|
|DIAGRAMJAVA-50492|Genişlik ve Yükseklik hücrelerindeki formüller korunmuyor|Böcek|
|DIAGRAMJAVA-50493|VSD'i SVG'e dönüştürürken eksik karakterler|Böcek|
|DIAGRAMJAVA-50494|Çıktı VSDX - işlem şekillerinin ortasında bağlantı hatları bağlanmıyor|Böcek|
|DIAGRAMJAVA-50499|VSDX ila PNG - şeklin altında beyaz bir yatay çizgi belirir|Böcek|
## **Herkese Açık API ve Geriye Dönük Uyumsuz Değişiklikler**
Eklenen, yeniden adlandırılan, kaldırılan veya kullanımdan kaldırılan üyeler gibi halka açık API'de yapılan tüm değişikliklerin yanı sıra Aspose.Diagram for Java'de yapılan geriye dönük uyumlu olmayan değişiklikler için listeye bakın. Listelenen herhangi bir değişiklikle ilgili endişeleriniz varsa, lütfen bunu[Aspose.Diagram destek forumu](https://forum.aspose.com/c/diagram/17).
### **Shape sınıfına freshData Yöntemi ekler**
Shape.refreshData yöntemi, geliştiricilerin şeklin konumunu, şeklin metnini, Geom'ları ve bağlantıları değiştirdikten sonra verileri yenilemesine olanak tanır.

{{< highlight "java" >}}

 // Call a Diagram class constructor to load the Visio drawing

Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

//Find a particular shape and update its XForm

for(Shape shape :(Iterable<Shape>) diagram.getPages().get(0).getShapes())

{

    if (shape.getNameU().toLowerCase() == "process" && shape.getID() == 1)

    {

        shape.getXForm().getPinX().setValue(5);

        shape.getXForm().getPinY().setValue(5);

        shape.refreshData();

    }

}

{{< /highlight >}}
