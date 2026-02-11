---
title: SolutionXML Öğeleriyle Çalışma
type: docs
weight: 110
url: /tr/net/working-with-solutionxml-elements/
description: Bu bölüm, solutionXml öğesinin nasıl ekleneceğini veya Aspose.Diagram ile solutionXml öğesinden xml değerlerinin nasıl alınacağını açıklar.
---
## **Visio Çizimine SolutionXML Öğesi Ekleyin**
 SolutionXML, kalıcı çözüm verileri için standartlaştırılmış bir araç sağlayan bir SolutionXML öğesinin içinde yer alan iyi biçimlendirilmiş XML'dir. Kullanıcılar, SolutionXML'i hemen VisioDocument öğesinde depolandığı Belge düzeyinde depolayabilir. Genellikle bu, SolutionXML'yi depolamanın ve almanın en kolay yoludur.[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).

 bu[ÇözümXML](http://www.aspose.com/api/net/diagram/aspose.diagram/solutionXML) class, Visio çizimlerinde SolutionXML öğesini temsil eder. Tarafından sunulan Add yöntemi[ÇözümXML](http://www.aspose.com/api/net/diagram/aspose.diagram/solutionXML) class, bir SolutionXML öğesi eklemeye izin verir.
### **SolutionXML Elemanı Programlama Örneği Ekleme**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_SolutionXML();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Initialize SolutionXML object
SolutionXML solXML = new SolutionXML();
// Set name
solXML.Name = "Solution XML";
// Set xml value
solXML.XmlValue = "XML Value";
// Add SolutionXML element
diagram.SolutionXMLs.Add(solXML);

// Save Visio diagram
diagram.Save(dataDir + "AddSolutionXMLElement_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **SolutionXML Öğesinden XML Değerlerini Okuma**
SolutionXML, kalıcı çözüm verileri için standartlaştırılmış bir araç sağlayan bir SolutionXML öğesinin içinde yer alan iyi biçimlendirilmiş XML'dir. Kullanıcılar, kullanarak SolutionXML öğesinden XML değerlerini okuyabilir.[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).

 Tarafından sunulan SolutionXMLs özelliği[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) sınıfı, Aspose.Diagram.SolutionXML nesne koleksiyonunu destekler. Bu özellik, SolutionXML öğesinden XML değerlerini okumak için kullanılabilir.
### **Okuma ÇözümüXML Elemanı Programlama Örneği**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_SolutionXML();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Iterate through SolutionXML elements
foreach (SolutionXML solutionXML in diagram.SolutionXMLs)
{
    // Get name property
    Console.WriteLine(solutionXML.Name);
    // Get xml value
    Console.WriteLine(solutionXML.XmlValue);
}

{{< /highlight >}}
```
