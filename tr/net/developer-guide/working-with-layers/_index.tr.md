---
title: Katmanlarla Çalışmak
type: docs
weight: 130
url: /tr/net/working-with-layers/
description: Bu bölümde, Aspose.Diagram ile visio şeklinde katman bilgilerinin nasıl ekleneceği veya alınacağı açıklanmaktadır.
---
## **Visio'de Şekil Nesnelerini Katmanlarla Yapılandırma**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) Microsoft Office Visio diagram'deki katmanlarla şekil nesnelerini yapılandırmaya izin verir. Her şekil birden çok katmana ait olabilir, böylece geliştiriciler son kullanıcı ihtiyaçlarına uygun şekilleri yönetebilir. bu[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class nesnesi, Visio çiziminde katmanlara şekil nesneleri eklemeye ve katmanlardan kaldırmaya izin veren LayerMember özelliğini sunar. Kullanıcılar bu özellikleri programlı olarak Aspose.Diagram API kullanarak aşağıdaki gibi yönetebilir:
### **Şekil Nesnelerini Yapılandırma Programlama Örneği**
Aşağıdaki kod parçası, şekil nesnesi özelliklerini eklemeye, kaldırmaya ve taşımaya yardımcı olur.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Layers();

// Load a source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");

// Iterate through the shapes
foreach (Aspose.Diagram.Shape shape in page.Shapes)
{
    if (shape.Name.ToLower() == "shape1")
    {
        // Add shape1 in first two layers. Here "0;1" are indexes of the layers
        LayerMem layer = shape.LayerMem;
        layer.LayerMember.Value = "0;1";
    }
    else if (shape.Name.ToLower() == "shape2")
    {
        // Remove shape2 from all the layers
        LayerMem layer = shape.LayerMem;
        layer.LayerMember.Value = "";
    }
    else if (shape.Name.ToLower() == "shape3")
    {
        // Add shape3 in first layer. Here "0" is index of the first layer
        LayerMem layer = shape.LayerMem;
        layer.LayerMember.Value = "0";
    }
}
// Save diagram
diagram.Save(dataDir + "ConfigureShapeLayers_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Visio Diagram'de yeni bir Katman ekleyin**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) geliştiricilerin özel şekil kategorilerini düzenlemek için yeni katmanlar eklemesine ve ardından bu katmanlara programlı olarak şekiller atamasına olanak tanır. bu[Katman Koleksiyonu](http://www.aspose.com/api/net/diagram/aspose.diagram/layercollection) class, yeni bir tane eklemeye izin veren Add yöntemini sunar.[Katman](http://www.aspose.com/api/net/diagram/aspose.diagram/layer) Visio çiziminde. Geliştiriciler, sınıf nesnesini başlatarak Katman özelliklerini ayarlayabilir.
### **Katman Programlama Örneği Ekle**
Aşağıdaki kod parçası, Katman nesneleri eklemeye yardımcı olur.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Layers();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// Initialize a new Layer class object
Layer layer = new Layer();
// Set Layer name
layer.Name.Value = "Layer1";
// Set Layer Visibility
layer.Visible.Value = BOOL.True;
// Set the color checkbox of Layer
layer.IsColorChecked = BOOL.True;
// Add Layer to the particular page sheet
page.PageSheet.Layers.Add(layer);

// Get shape by ID
Shape shape = page.Shapes.GetShape(3);
// Assign shape to this new Layer
shape.LayerMem.LayerMember.Value = layer.IX.ToString();
// Save diagram
diagram.Save(dataDir + "AddLayer_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Visio Diagram'den Tüm Katmanları Alın**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) Visio diagram'in mevcut katmanlarını almak için geliştiricilere erişim sağlar.[Sayfa Sayfası](http://www.aspose.com/api/net/diagram/aspose.diagram/pagesheet) mülkiyeti[Sayfa](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class, kullanarak bir Visio diagram'den kullanılabilir katmanların listesini almaya izin verir.[Katman Koleksiyonu](http://www.aspose.com/api/net/diagram/aspose.diagram/layercollection) sınıf.
### **Katman Programlama Örneği Al**
Aşağıdaki kod parçası, Katmanların listesini almanıza yardımcı olur.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Layers();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// Iterate through the layers
foreach (Layer layer in page.PageSheet.Layers)
{
    Console.WriteLine("Name: " + layer.Name.Value);
    Console.WriteLine("Visibility: " + layer.Visible.Value);
    Console.WriteLine("Status: " + layer.Status.Value);
}

{{< /highlight >}}

