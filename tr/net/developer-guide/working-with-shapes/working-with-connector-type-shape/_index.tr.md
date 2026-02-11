---
title: Konnektör Tipi Şekil ile Çalışma
type: docs
weight: 70
url: /tr/net/working-with-connector-type-shape/
description: Bu bölümde Konektör Görünümünün Aspose.Diagram ile nasıl ayarlanacağı açıklanmaktadır.
---
## **Visio'de Konektör Türü Şeklinin Görünümünü Ayarlayın**
Bu konuda, geliştiricilerin Aspose.Diagram for .NET'i kullanarak dinamik bağlayıcı türü şeklinin görünümünü nasıl değiştirebilecekleri açıklanmaktadır.
### **Bağlayıcı Görünümünü Ayarla**
 Tarafından sunulan SetConnectorsType yöntemi[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class, bağlayıcı türü şeklinin görünümünü ayarlamak için kullanılabilir.

Aşağıdaki kod nasıl yapılacağını gösterir:

1. Bir numune yükleyin diagram.
1. belirli bir sayfa alın.
1. belirli bir konektör şekli elde edin.
1. şeklin görünümünü ayarlayın.
1. kaydet diagram
#### **Bağlayıcı Görünümü Programlama Örneği Ayarla**
Aspose.Diagram for .NET kullanarak konektör tipi şeklinin görünümünü ayarlamak için .NET uygulamanızda aşağıdaki kodu kullanın.


{{< highlight csharp >}}
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

## **Bağlayıcı Şeklinin Yeniden Yönlendirme Seçeneğini Belirleyin**
 Tarafından sunulan ConFixedCode özelliği[Düzen](http://www.aspose.com/api/net/diagram/aspose.diagram/layout) sınıf, yeniden yönlendirme seçeneğini seçmek için kullanılabilir. tarafından sunulan Layout özelliği[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) sınıf kullanılacaktır.

Aşağıdaki kod nasıl yapılacağını gösterir:

1. Bir örnek dosya yükleyin.
1. belirli bir sayfa alın.
1. belirli bir konektör şekli elde edin.
1. yeniden yönlendirme seçeneklerini ayarlayın.
1. diagram'i kaydedin.
### **Yeniden Yönlendirme Seçeneği Programlama Örneği Seçin**
Aspose.Diagram for .NET kullanarak bağlayıcı şeklinin yeniden yönlendirme seçeneğini belirlemek için .NET uygulamanızda aşağıdaki kodu kullanın.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

// Get a particular connector shape
Shape shape = page.Shapes.GetShape(18);
// Set reroute option
shape.Layout.ConFixedCode.Value = ConFixedCodeValue.NeverReroute;

// Save Visio diagram
diagram.Save(dataDir + "RerouteConnectors_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

