---
title: Visio Şeklini Html'ye Dönüştür
type: docs
weight: 10
url: /tr/net/convert-a-visio-shape-to-html/
description: Bu bölümde, visio şeklinin Aspose.Diagram ile html'ye nasıl dönüştürüleceği açıklanmaktadır.
---
## ** visio şeklini html'ye dönüştürün**
 Tarafından sunulan ToHTML yöntemi[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class, html'ye dönüştürmek için kullanılabilir.

Aşağıdaki kod nasıl yapılacağını gösterir:

1. Bir numune yükleyin diagram.
1. belirli bir sayfa alın.
1. Belirli bir şekil elde edin.
1. şekli html'ye dönüştürün.
### **Html'ye Şekil Ver**
visio şeklini html'ye dönüştürmek için .net uygulamanızda aşağıdaki kodu kullanın.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToHtml.vsdx");

// Get a particular page
Page page = diagram.Pages[0];

// Get a particular shape
Shape shape = page.Shapes[0];

// Shape to HTML
Aspose.Diagram.Saving.HTMLSaveOptions hs = new Aspose.Diagram.Saving.HTMLSaveOptions();
shape.ToHTML("out.htm", hs);

{{< /highlight >}}


