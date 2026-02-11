---
title: Şekil verilerini yenile
type: docs
weight: 40
url: /tr/net/refresh-shapes-data/
description: Bu bölümde, visio şekli için şekil verilerinin Aspose.Diagram ile nasıl yenileneceği açıklanmaktadır.
---
## **Şeklin metnini veya diğerini değiştirirken xform ,connection ve geom dahil olmak üzere şeklin konumunu yeniler**
 Tarafından sunulan RefreshData yöntemi[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) sınıf, şeklin verilerini yenilemek için kullanılabilir

Aşağıdaki kod nasıl yapılacağını gösterir:

1. Bir örnek dosya yükleyin.
1. Belirli bir şekle erişin.
1. Şeklin verilerini yenileyin.
### **Shape'in verilerini yenile**
Aspose.Diagram for .NET kullanarak bir şekli yenilemek için .NET uygulamanızda aşağıdaki kodu kullanın.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

// Get Shape
Shape shape = page.Shapes.GetShape(15);

// Refresh data
shape.RefreshData();

// Save visio diagram
diagram.Save(dataDir + "RefreshData_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


