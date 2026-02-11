---
title: Visio Şekil Devralma Satırını Alın
type: docs
weight: 100
url: /tr/net/get-visio-shape-inherit-line/
description: Bu bölüm, visio şeklinin üst stilinden devralınan çizgi stilini ve Aspose.Diagram ile ana stilini nasıl alacağınızı açıklar.
---
### **Visio Şeklinin Miras Alınan Satır Verilerini Alma**
 Visio şekilleri, ana stili ve ana şekli devralabilir. Geliştiriciler, bir Visio şeklinin devralma satırı verilerini alabilir veya ayarlayabilir. Tarafından sunulan InheritLine özelliği[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class, üst stil ve ana şekil tarafından devralınan şeklin çizgi formatlama değerlerini içerir.
#### **Miras Alınan Satır Verilerini Al Programlama Örneği**
Aşağıdaki kod parçacığı, şeklin devralınan çizgi verilerini alır. Lütfen bu örnek kodu kontrol edin:


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

foreach (Aspose.Diagram.Shape shape in page.Shapes)
{
	Line line = shape.InheritLine;
	Console.WriteLine(line.LinePattern.Value);
	Console.WriteLine(line.LineColor.Value);
	Console.WriteLine(line.BeginArrow.Value);
	Console.WriteLine(line.BeginArrowSize.Value);
	Console.WriteLine(line.EndArrow.Value);
	Console.WriteLine(line.EndArrowSize.Value);
	Console.WriteLine(line.LineWeight.Value);
}

{{< /highlight >}}


