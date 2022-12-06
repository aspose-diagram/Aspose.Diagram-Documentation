---
title: Java üzerinden Python için Aspose.Diagram 22.6 Sürüm Notları
type: docs
weight: 22
url: /tr/java/aspose-diagram-for-python-via-java-22-6-release-notes/
---
{{% alert color="primary" %}}

Bu sayfa, Java 22.6 üzerinden Python için Aspose.Diagram için sürüm notları bilgilerini içerir.

{{% /alert %}}
## **İyileştirmeler ve Değişiklikler**  ##

|**Anahtar**|**Özet**|**Kategori**|
|:- |:- |:- |
|DIAGRAMJAVA-50963|WK: PNG'ye kaydettikten sonra şekil bozuk|Artırma|
|DIAGRAMJAVA-50967|Yanal çizgi şeklini yeniden boyutlandırma [Devam]|Böcek|
|DIAGRAMJAVA-50972|API dosyayı doğru şekilde ayrıştırmıyor|Böcek|
|DIAGRAMJAVA-50974|Yeni bağlantı noktası ekleme sorunu|Böcek|

## `?`**Genel API ve Geriye Dönük Uyumsuz Değişiklikler**
Aşağıda, API numaralı telefon numarasına eklenen, yeniden adlandırılan, kaldırılan veya kullanımdan kaldırılan üyeler gibi genele açık olarak yapılan tüm değişikliklerin ve Aspose.Diagram for Java numaralı telefona yapılan geriye dönük uyumlu olmayan değişikliklerin bir listesi bulunmaktadır. Listelenen herhangi bir değişiklikle ilgili endişeleriniz varsa lütfen şu adrese bildirin: Aspose.Diagram destek forumu.

### **HTMLSaveOptions'a Çözünürlük Ekler**
- Oluşturulan html için çözünürlüğü inç başına nokta cinsinden alır veya ayarlar

{{< highlight "java" >}}
HTMLSaveOptions option = new HTMLSaveOptions();
option.setResolution(96);
{{< /highlight >}}
