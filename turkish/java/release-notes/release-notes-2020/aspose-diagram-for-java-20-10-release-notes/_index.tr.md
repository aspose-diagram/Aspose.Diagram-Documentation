---
title: Aspose.Diagram for Java 20.10 Sürüm Notları
type: docs
weight: 10
url: /tr/java/aspose-diagram-for-java-20-10-release-notes/
---
{{% alert color="primary" %}}

Bu sayfa Aspose.Diagram for Java 20.10 için sürüm notları bilgilerini içerir.

{{% /alert %}}
## **İyileştirmeler ve Değişiklikler**  ##

|**Anahtar**|**Özet**|**Kategori**|
|:- |:- |:- |
|DIAGRAMJAVA-50457|Bir VSD sayfası SVG'lere dönüştürülürken metin öğelerinin yeri değiştiriliyor|Artırma|

## Genel API Değişiklikler
* SVGSaveOptions'a IsExportScaleInMatrix eklendi - Matriste dışa aktarma ölçeğine gerek olup olmadığını tanımlar.
```
SVGSaveOptions o = new SVGSaveOptions();
o.setExportScaleInMatrix(false);
```
