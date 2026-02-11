---
title: Visio Şeklini Pdf'ye Dönüştür
type: docs
weight: 10
url: /tr/java/convert-a-visio-shape-to-pdf/
description: Bu bölümde, visio şeklinin Aspose.Diagram ile pdf'ye nasıl dönüştürüleceği açıklanmaktadır.
---
## ** visio şeklini pdf'ye dönüştür**
 Tarafından sunulan ToPdf yöntemi[Şekil](http://www.aspose.com/api/java/diagram/com.aspose.diagram/shape) sınıf, pdf'ye dönüştürmek için kullanılabilir.

Aşağıdaki kod nasıl yapılacağını gösterir:

1. Bir numune yükleyin diagram.
1. belirli bir sayfa alın.
1. Belirli bir şekil elde edin.
1. şekli pdf'ye dönüştür.
### **Pdf'ye Şekil Ver**
Bir visio şeklini pdf'ye dönüştürmek için java uygulamanızda aşağıdaki kodu kullanın.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ShapeToPdf.class); 
// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToPdf.vsdx");

// Get a particular page
Page page = diagram.getPages().get(0);

// Get a particular shape
Shape shape = page.getShapes().get(0);

// Shape to Pdf
shape.toPdf("out.pdf");
{{< /highlight >}}



