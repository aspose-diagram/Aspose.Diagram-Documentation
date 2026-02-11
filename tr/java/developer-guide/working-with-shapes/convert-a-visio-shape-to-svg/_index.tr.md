---
title: Visio Şeklini Svg'ye Dönüştür
type: docs
weight: 10
url: /tr/java/convert-a-visio-shape-to-svg/
description: Bu bölümde, visio şeklinin Aspose.Diagram ile svg'ye nasıl dönüştürüleceği açıklanmaktadır.
---
## ** visio şeklini svg'ye dönüştürme**
 Tarafından sunulan ToSvg yöntemi[Şekil](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) sınıf, svg'ye dönüştürmek için kullanılabilir.

Aşağıdaki kod nasıl yapılacağını gösterir:

1. Bir numune yükleyin diagram.
1. belirli bir sayfa alın.
1. Belirli bir şekil elde edin.
1. şekli svg'ye dönüştür.
### **Svg'ye Şekil Ver**
Bir visio şeklini svg'ye dönüştürmek için java uygulamanızda aşağıdaki kodu kullanın.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ShapeToSvg.class); 
// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToSvg.vsdx");

// Get a particular page
Page page = diagram.getPages().get(0);

// Get a particular shape
Shape shape = page.getShapes().get(0);

// Shape to Svg
SVGSaveOptions option = new SVGSaveOptions();
shape.toSvg("out.svg",option);
{{< /highlight >}}
```


