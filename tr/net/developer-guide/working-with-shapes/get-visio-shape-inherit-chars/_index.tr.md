---
title: Visio Şekil Devralma Karakterlerini Alın
type: docs
weight: 101
url: /tr/net/get-visio-shape-inherit-chars/
description: Bu bölüm, visio şeklinin ana stilinden ve Aspose.Diagram ana stilinden devralınan yazı tipi stilinin nasıl alınacağını açıklar.
---
### **Visio Şeklinin Miras Alınan Yazı Tipi Verilerini Alma**
 Visio şekilleri, ana stili ve ana şekli devralabilir. Geliştiriciler, bir Visio şeklinin miras alınan yazı tipi verilerini alabilir veya ayarlayabilir. Tarafından sunulan InheritLine özelliği[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class, üst stil ve ana şekil tarafından devralınan şeklin çizgi formatlama değerlerini içerir.
#### **Miras Alınan Yazı Tipi Verilerini Al Programlama Örneği**
Aşağıdaki kod parçacığı, şeklin devralınan yazı tipi verilerini alır. Lütfen bu örnek kodu kontrol edin:


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
	Aspose.Diagram.Char ch = shape.InheritChars.GetChar(0);
	Console.WriteLine(ch.Style.Value);
	Console.WriteLine(ch.Color.Value); 
	Console.WriteLine(ch.FontName.Value); 
	Console.WriteLine(ch.Size.Value);
	Console.WriteLine(ch.Case.Value);
	Console.WriteLine(ch.IsUnderline);
	Console.WriteLine(ch.IsItalic);
	Console.WriteLine(ch.IsStrikethrough);
	Console.WriteLine(ch.IsDoubleStrikethrough);
	Console.WriteLine(ch.IsSubscript);
	Console.WriteLine(ch.IsSuperscript); 
}

{{< /highlight >}}


