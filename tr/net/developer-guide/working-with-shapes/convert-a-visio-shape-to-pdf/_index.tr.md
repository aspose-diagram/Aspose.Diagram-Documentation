---
title: Visio Şeklini Pdf'ye Dönüştür
type: docs
weight: 10
url: /tr/net/convert-a-visio-shape-to-pdf/
description: Bu bölümde, visio şeklinin Aspose.Diagram ile pdf'ye nasıl dönüştürüleceği açıklanmaktadır.
---
## ** visio şeklini pdf'ye dönüştür**
 Tarafından sunulan ToPdf yöntemi[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) sınıf, pdf'ye dönüştürmek için kullanılabilir.

Aşağıdaki kod nasıl yapılacağını gösterir:

1. Bir numune yükleyin diagram.
1. belirli bir sayfa alın.
1. Belirli bir şekil elde edin.
1. şekli pdf'ye dönüştür.
### **Pdf'ye Şekil Ver**
visio şeklini pdf'ye dönüştürmek için .net uygulamanızda aşağıdaki kodu kullanın.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToPdf.vsdx");

// Get a particular page
Page page = diagram.Pages[0];

// Get a particular shape
Shape shape = page.Shapes[0];

// Shape to Pdf
shape.ToPdf("out.pdf");

{{< /highlight >}}


