---
title: SolutionXML Öğeleriyle Çalışma
type: docs
weight: 140
url: /tr/java/working-with-solutionxml-elements/
---
## **Visio Çizimine SolutionXML Öğesi Ekleyin**
 SolutionXML, kalıcı çözüm verileri için standartlaştırılmış bir araç sağlayan bir SolutionXML öğesinin içinde yer alan iyi biçimlendirilmiş XML'dir. Kullanıcılar, SolutionXML'i hemen VisioDocument öğesinde depolandığı Belge düzeyinde depolayabilir. Genellikle bu, SolutionXML'yi depolamanın ve almanın en kolay yoludur.[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).

 bu[ÇözümXML](https://reference.aspose.com/diagram/java/com.aspose.diagram/SolutionXML) class, Visio çizimlerinde SolutionXML öğesini temsil eder. Tarafından sunulan Add yöntemi[ÇözümXML](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/SolutionXML) class, bir SolutionXML öğesi eklemeye izin verir.
### **SolutionXML Elemanı Programlama Örneği Ekleme**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AddSolutionXMLElement.class);  
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// initialize SolutionXML object
SolutionXML solXML = new SolutionXML();
// set name
solXML.setName("Solution XML");
// set xml value
solXML.setXmlValue("XML Value");
// add SolutionXML element
diagram.getSolutionXMLs().add(solXML);

// save Visio diagram
diagram.save(dataDir + "AddSolutionXMLElement_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **SolutionXML Öğesinden XML Değerlerini Okuma**
SolutionXML, kalıcı çözüm verileri için standartlaştırılmış bir araç sağlayan bir SolutionXML öğesinin içinde yer alan iyi biçimlendirilmiş XML'dir. Kullanıcılar, kullanarak SolutionXML öğesinden XML değerlerini okuyabilir.[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).

 Tarafından sunulan SolutionXMLs özelliği[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) sınıfı, Aspose.Diagram.SolutionXML nesne koleksiyonunu destekler. Bu özellik, SolutionXML öğesinden XML değerlerini okumak için kullanılabilir.
### **Okuma ÇözümüXML Elemanı Programlama Örneği**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ReadSolutionXMLElement.class);   
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// iterate through SolutionXML elements
for (SolutionXML solutionXML :(Iterable<SolutionXML>) diagram.getSolutionXMLs())
{
    // get name property
    System.out.println(solutionXML.getName());
    // get xml value
    System.out.println(solutionXML.getXmlValue());
}

{{< /highlight >}}

