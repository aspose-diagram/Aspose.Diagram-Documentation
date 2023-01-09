﻿---
title: Node.js için Aspose.Diagram via Java 22.3 Sürüm Notları
type: docs
weight: 25
url: /tr/java/aspose-diagram-for-node-js-via-java-22-3-release-notes/
---
{{% alert color="primary" %}}

Bu sayfa, Node.js via Java 22.3 için Aspose.Diagram sürüm notları bilgilerini içerir.

{{% /alert %}}
## **İyileştirmeler ve Değişiklikler**  ##

|**Anahtar**|**Özet**|**Kategori**|
|:- |:- |:- |
|DIAGRAMJAVA-50883|API numaralı telefondan eksik yazı tiplerini ve yazı tipi değiştirme bilgilerini belirleyin|Böcek|

## `?`**Genel API ve Geriye Dönük Uyumsuz Değişiklikler**
Aşağıda, API numaralı telefon numarasına eklenen, yeniden adlandırılan, kaldırılan veya kullanımdan kaldırılan üyeler gibi genele açık olarak yapılan tüm değişikliklerin ve Aspose.Diagram for Java numaralı telefona yapılan geriye dönük uyumlu olmayan değişikliklerin bir listesi bulunmaktadır. Listelenen herhangi bir değişiklikle ilgili endişeleriniz varsa lütfen şu adrese bildirin: Aspose.Diagram destek forumu.

### **AddText'i Sayfaya Ekler**
- Tanımlı PinX ve PinY ile Metin ekler.

{{< highlight "java" >}}
Shape shape = page.addText(1, 1, 2, 2, "Test text", "Calibri", "#a5a5a5", 0.25);
{{< /highlight >}}