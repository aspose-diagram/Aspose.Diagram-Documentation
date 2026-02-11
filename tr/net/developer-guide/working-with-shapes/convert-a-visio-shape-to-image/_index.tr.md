---
title: Visio Şeklini Görüntüye Dönüştür
type: docs
weight: 10
url: /tr/net/convert-a-visio-shape-to-image/
description: Bu bölümde, visio şeklinin Aspose.Diagram ile görüntüye nasıl dönüştürüleceği açıklanmaktadır.
---
## **visio şeklini resme dönüştürün**
Bu konu, geliştiricilerin bir visio şeklini Aspose.Diagram kullanarak görüntüye nasıl dönüştürebileceğini ayrıntılı olarak açıklar.
 Tarafından sunulan ToImage yöntemi[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) sınıf görüntüye dönüştürmek için kullanılabilir.


Aşağıdaki kod nasıl yapılacağını gösterir:

1. Bir numune yükleyin diagram.
1. belirli bir sayfa alın.
1. Belirli bir şekil elde edin.
1. şekli görüntüye dönüştürün.
#### **Şekilden görüntüye Programlama Örneği**
visio şeklini görüntüye dönüştürmek için .net uygulamanızda aşağıdaki kodu kullanın.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToImage.vsdx");

// Get a particular page
Page page = diagram.Pages[0];

// Get a particular shape
Shape shape = page.Shapes[0];

// Shape to Image
Aspose.Diagram.Saving.ImageSaveOptions o = new Aspose.Diagram.Saving.ImageSaveOptions(SaveFileFormat.PNG);
shape.ToImage("out.png", o);

{{< /highlight >}}
```
