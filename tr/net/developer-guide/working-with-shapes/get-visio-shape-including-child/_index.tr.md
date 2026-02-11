---
title: Al Visio Şekil Çocuk Dahil
type: docs
weight: 110
url: /tr/net/get-visio-shape-including-child/
description: Bu bölümde, Aspose.Diagram ile şeklin kimliği veya adı olan çocuk da dahil olmak üzere visio şeklinin nasıl alınacağı açıklanmaktadır.
---
### **Visio Şekli İçeren Alt Öğeyi Alın**
diagram'deki her şeklin bir kimliği ve adı vardır. Kimlik, Visio ile programlama yaparken önemlidir: bir şekle erişmenin ana yöntemidir. Her şekil ayrıca hangi kalıptan (şablondan) yapıldığına dair bilgileri de tutar.

 A[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Visio çiziminde muhtemelen bir baba veya oğulları olan bir nesnedir. Page sınıfı tarafından sunulan Shapes özelliği, Aspose.Diagram.Shape nesne koleksiyonunu destekler. Shapes özelliği, bir şekil hakkında bilgi almak için kullanılabilir.
#### **Visio Şekil Programlama Örneği'ni alın**
Aşağıdaki kod parçacığı, alt öğeyi içeren şekli alır. Lütfen bu örnek kodu kontrol edin:


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "NetworkConnection.vsdx");

Page page = diagram.Pages[0];

Shape shapeContainerChild = page.Shapes.GetShapeIncludingChild("RectangleChild");

if (shapeContainerChild == null)
    throw new Exception();
    
// Save visio diagram
diagram.Save(dataDir + "GroupShapes_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


