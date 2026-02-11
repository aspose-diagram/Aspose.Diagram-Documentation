---
title: Döndür Visio Şekil Metni
type: docs
weight: 9
url: /tr/net/rotate-visio-shape-text/
keywords: Rotate, visio, Tex
description: .NET Diagram API kullanılarak visio'de şeklin metni nasıl döndürülür.
---
## **Diagram oluşturma**
 Aspose.Diagram for .NET, Microsoft Office Otomasyon olmadan kendi uygulamalarınız içinden Microsoft Visio diyagramlarını okumanızı ve oluşturmanızı sağlar. Yeni belgeler oluştururken ilk adım, bir diagram oluşturmaktır. Ardından[şekiller ve bağlayıcılar ekleyin](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/)diagram'i oluşturmak için.[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) yeni bir diagram oluşturmak için sınıf.
### **Programlama Örneği**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Create directory if it is not already present.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// Initialize a new Visio
Diagram diagram = new Diagram();
dataDir = dataDir + "CreateDiagram_out.vsdx";
// Save in the VSDX format
diagram.Save(dataDir, SaveFileFormat.VSDX);

{{< /highlight >}}
```

Bu örnek şu şekilde çalışır:

1. Diagram sınıfından bir nesne oluşturun.
1. Belirli bir sayfa al
1. Belirli bir şekle sahip olun
1. Şekil metnini alın ve metni döndürün
1. Diagram sınıf nesnesinin Kaydetme yöntemini çağırın ve ayrıca tam dosya yolunu ve DiagramSaveOptions nesnesini iletin.
### **Metni döndürme Programlama Örneği**
Aşağıdaki örnek kod, Visio diagram'deki metnin nasıl döndürüleceğini gösterir.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeText();

// Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir + "UpdateShapeText.vsd");
// Get page by name
Page page = diagram.Pages.GetPage("Flow 1");
// Find a particular shape and update its text
foreach (Aspose.Diagram.Shape shape in page.Shapes)
{
    if (shape.NameU.ToLower() == "process" && shape.ID == 1)
    {
        shape.Text.Value.Clear();
        shape.Text.Value.Add(new Txt("New Text"));
        // Set orientation angle
        double angleDeg = 90;
        double angleRad = (Math.PI / 180) * angleDeg;
        shape.TextXForm.TxtAngle.Value = angleRad;
    }
}
// Save diagram
diagram.Save(dataDir + "UpdateShapeText_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
