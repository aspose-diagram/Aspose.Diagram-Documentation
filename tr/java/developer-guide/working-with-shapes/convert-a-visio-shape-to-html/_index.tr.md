---
title: Visio Şeklini Html'ye Dönüştür
type: docs
weight: 10
url: /tr/java/convert-a-visio-shape-to-html/
description: Bu bölümde, visio şeklinin Aspose.Diagram ile html'ye nasıl dönüştürüleceği açıklanmaktadır.
---
## ** visio şeklini html'ye dönüştürün**
 Tarafından sunulan ToHTML yöntemi[Şekil](http://www.aspose.com/api/java/diagram/com.aspose.diagram/shape) class, html'ye dönüştürmek için kullanılabilir.

Aşağıdaki kod nasıl yapılacağını gösterir:

1. Bir numune yükleyin diagram.
1. belirli bir sayfa alın.
1. Belirli bir şekil elde edin.
1. şekli html'ye dönüştürün.
### **Html'ye Şekil Ver**
Bir visio şeklini html'ye dönüştürmek için java uygulamanızda aşağıdaki kodu kullanın.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ShapeToHtml.class); 
// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToHtml.vsdx");

// Get a particular page
Page page = diagram.getPages().get(0);

// Get a particular shape
Shape shape = page.getShapes().get(0);

// Shape to HTML
HTMLSaveOptions hs = new HTMLSaveOptions();
shape.toHTML("out.htm", hs);
{{< /highlight >}}
```


