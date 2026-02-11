---
title: Visio Şeklini Svg'ye Dönüştür
type: docs
weight: 10
url: /tr/net/convert-a-visio-shape-to-svg/
description: Bu bölümde, visio şeklinin Aspose.Diagram ile svg'ye nasıl dönüştürüleceği açıklanmaktadır.
---
## ** visio şeklini svg'ye dönüştürme**
 Tarafından sunulan ToSvg yöntemi[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) sınıf, svg'ye dönüştürmek için kullanılabilir.

Aşağıdaki kod nasıl yapılacağını gösterir:

1. Bir numune yükleyin diagram.
1. belirli bir sayfa alın.
1. Belirli bir şekil elde edin.
1. şekli svg'ye dönüştür.
### **Svg'ye Şekil Ver**
visio şeklini svg'ye dönüştürmek için .net uygulamanızda aşağıdaki kodu kullanın.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToSvg.vsdx");

// Get a particular page
Page page = diagram.Pages[0];

// Get a particular shape
Shape shape = page.Shapes[0];

SVGSaveOptions svgOptions = new SVGSaveOptions();
// Shape to Svg
shape.ToSvg("out.svg",svgOptions);

{{< /highlight >}}


