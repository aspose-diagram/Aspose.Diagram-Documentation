---
title: Şekle Bağlantı Noktası Ekle
type: docs
weight: 70
url: /tr/net/add-connection-point-to-shape/
description: Bu bölüm, Aspose.Diagram ile visio şekline bağlantı noktasının nasıl ekleneceğini açıklar.
---
## **Visio'de Şekle Bağlantı Noktası Ekleme**
Bu konu, geliştiricilerin Aspose.Diagram for .NET'i kullanarak bir visio şekline nasıl bağlantı noktası ekleyebileceğini açıklamaktadır.
### **Bağlantı Noktası Ekle**
 bu[Bağlantılar](https://reference.aspose.com/diagram/net/aspose.diagram/shape/properties/connections) nesne, içindeki bağlantı koleksiyonunu temsil eder.[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) sınıf.

Aşağıdaki kod nasıl yapılacağını gösterir:

1. Bir numune yükleyin diagram.
1. belirli bir sayfa alın.
1. Belirli bir şekil elde edin.
1. yeni bir bağlantı
1.  bağlantı özelliğini ayarla
1. şekle bağlantı ekle
1. kaydet diagram
#### **Programlama Örneğini şekillendirmek için bağlantı noktası ekleyin**
.NET for .NET kullanarak bir şekle bağlantı eklemek için .NET uygulamanızda aşağıdaki kodu kullanın.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsd");

// Get a particular page
Page page = diagram.Pages.GetPage("Page-3");
// Get a dynamic connector type shape by id
Shape shape = page.Shapes.GetShape(18);
// Set dynamic connector appearance
shape.SetConnectorsType(ConnectorsTypeValue.StraightLines);

// Saving Visio diagram
diagram.Save(dataDir + "SetConnectorAppearance_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
