---
title: Visio Şeklini Görüntüye Dönüştür
type: docs
weight: 10
url: /tr/java/convert-a-visio-shape-to-image/
description: Bu bölümde, visio şeklinin Aspose.Diagram ile görüntüye nasıl dönüştürüleceği açıklanmaktadır.
---
## **visio şeklini resme dönüştürün**
 Tarafından sunulan ToImage yöntemi[Şekil](http://www.aspose.com/api/java/diagram/com.aspose.diagram/shape) sınıf görüntüye dönüştürmek için kullanılabilir.

Aşağıdaki kod nasıl yapılacağını gösterir:

1. Bir numune yükleyin diagram.
1. belirli bir sayfa alın.
1. Belirli bir şekil elde edin.
1. şekli görüntüye dönüştürün.
### **Şekilden Görüntüye**
visio şeklini görüntüye dönüştürmek için java uygulamanızda aşağıdaki kodu kullanın.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ShapeToImage.class); 
// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToImage.vsdx");

// Get a particular page
Page page = diagram.getPages().get(0);

// Get a particular shape
Shape shape = page.getShapes().get(0);

// Shape to image
com.aspose.diagram.ImageSaveOptions option = new com.aspose.diagram.ImageSaveOptions(SaveFileFormat.PNG);
shape.toImage("out.png",option);
{{< /highlight >}}



