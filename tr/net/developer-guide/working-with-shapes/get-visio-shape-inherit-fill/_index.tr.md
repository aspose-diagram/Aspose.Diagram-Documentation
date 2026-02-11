---
title: Visio Şekil Devralma Dolgusunu Alın
type: docs
weight: 100
url: /tr/net/get-visio-shape-inherit-fill/
description: Bu bölüm, visio şeklinin ana stilinden ve Aspose.Diagram ana stilinden devralınan dolgu stilinin nasıl alınacağını açıklar.
---
### **Visio Şeklinin Miras Alınan Dolgu Verilerini Alma**
Visio şekilleri, ana stili ve ana şekli devralabilir. Geliştiriciler, bir Visio şeklinin devralınan Dolgu verilerini alabilir. Tarafından sunulan InheritFill özelliği[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class, ana stil ve ana şekil tarafından devralınan şeklin dolgu biçimlendirme değerlerini içerir.
#### **Devralınan Doldurma Verilerini Al Programlama Örneği**
Aşağıdaki kod parçacığı, şeklin devralınan dolgu verilerini alır. Lütfen bu örnek kodu kontrol edin:


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
	Fill f = shape.InheritFill;
	Console.WriteLine(f.FillForegnd.Value);
	Console.WriteLine(f.FillPattern.Value);
	Console.WriteLine(f.ShdwForegnd.Value);
	Console.WriteLine(f.ShdwPattern.Value);
}

{{< /highlight >}}


