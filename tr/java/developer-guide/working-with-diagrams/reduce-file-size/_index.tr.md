---
title: Dosya Boyutunu Küçült
type: docs
weight: 50
url: /tr/java/reduce-file-size/
description: Bu bölüm, dosya boyutunu diagram'den Aspose.Diagram ile nasıl küçülteceğinizi açıklar.
---
## **Dosya Boyutunu Küçült**
 Aspose.Diagram for Java API, geliştiricilerin dosya boyutunu azaltmak için bir diagram'den gizli bilgileri kaldırmasına olanak tanır.
 bu[Sayfa](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) nesne, bir ön plan sayfasının veya bir arka plan sayfasının çizim alanını temsil eder. Dosya boyutunu küçültmek için şunu kullanabilirsiniz:[Gizli Bilgi Öğesini Kaldır](https://reference.aspose.com/diagram/java/com.aspose.diagram/RemoveHiddenInfoItem) özellikleri**Gizli Bilgileri Kaldır()** yöntemi[Diagram](https://reference.aspose.com/diagram/java)sınıf. Aşağıdaki kod örneği, gizli bilgilerin diagram'den nasıl kaldırılacağını gösterir.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ReduceFileSize.class);

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Remove hidden information from diagram
diagram.removeHiddenInformation((int)(RemoveHiddenInfoItem.SHAPES | RemoveHiddenInfoItem.MASTERS));
{{< /highlight >}}

