---
title: Java 22.11 Sürüm Notları aracılığıyla Node.js için Aspose.Diagram
type: docs
weight: 17
url: /tr/nodejsjava/aspose-diagram-for-node-js-via-java-22-11-release-notes/
---
{{% alert color="primary" %}}

Bu sayfa, Java 22.11 üzerinden Node.js için Aspose.Diagram sürüm notları bilgilerini içerir.

{{% /alert %}}
## **İyileştirmeler ve Değişiklikler**  ##

|**Anahtar**|**Özet**|**Kategori**|
|:- |:- |:- |
|DIAGRAMJAVA-51049|Bir şekildeki bir çizginin bağlantı noktası nasıl elde edilir|Artırma|
|DIAGRAMJAVA-51044|.getDisplayText() html varlıklarının kodunu çözmek için (Aspose.Diagram Java 22.10, .vsd dosyaları)|Artırma|
|DIAGRAMJAVA-51046|Şeklin adı bazen Visio'deki adlardan farklıdır.|Böcek|

## **Herkese Açık API ve Geriye Dönük Uyumsuz Değişiklikler**
Aşağıda, API numaralı telefon numarasına eklenen, yeniden adlandırılan, kaldırılan veya kullanımdan kaldırılan üyeler gibi genele açık olarak yapılan tüm değişikliklerin ve Aspose.Diagram for Java numaralı telefona yapılan geriye dönük uyumlu olmayan değişikliklerin bir listesi bulunmaktadır. Listelenen herhangi bir değişiklikle ilgili endişeleriniz varsa lütfen şu adrese bildirin: Aspose.Diagram destek forumu.

### **Şekle getConnectorRule ekler**
- Şekle bağlı olan şekil kimliğini ve bağlantıyı içeren bir connectorRule döndürür

{{< highlight "java" >}}
ConnectorRule rule= shape.getConnectorRule();
{{< /highlight >}}

### **SVGSaveOptions'a setSavingCustomLinePattern ekler**
- Özel çizgi deseninin kaydedilip kaydedilmediğini tanımlar.

{{< highlight "java" >}}
SVGSaveOptions saveOp = new SVGSaveOptions(); 
saveOp.setSavingCustomLinePattern(false);
{{< /highlight >}}
