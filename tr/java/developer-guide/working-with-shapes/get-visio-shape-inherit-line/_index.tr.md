---
title: Visio Şekil Devralma Satırını Alın
type: docs
weight: 100
url: /tr/java/get-visio-shape-inherit-line/
description: Bu bölüm, visio şeklinin üst stilinden devralınan çizgi stilini ve Aspose.Diagram ile ana stilini nasıl alacağınızı açıklar.
---
### **Visio Şeklinin Miras Alınan Satır Verilerini Alma**
 Visio şekilleri, ana stili ve ana şekli devralabilir. Geliştiriciler, bir Visio şeklinin devralma satırı verilerini alabilir veya ayarlayabilir. Tarafından sunulan InheritLine özelliği[Şekil](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class, üst stil ve ana şekil tarafından devralınan şeklin çizgi formatlama değerlerini içerir.
#### **Miras Alınan Satır Verilerini Al Programlama Örneği**
Aşağıdaki kod parçacığı, şeklin devralınan çizgi verilerini alır. Lütfen bu örnek kodu kontrol edin:


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveInheritedLine.class) + "Shapes/";

// Call the diagram constructor to load a VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get page by ID
Page page = diagram.getPages().getPage("Page-1");
// Get shape by ID
Shape shape = page.getShapes().getShape(1);
//Get Inherit Line from the parent style and master
Line line = shape.getInheritLine();
// Get the line formatting values
System.out.println(line.getBeginArrow().getValue());
System.out.println(line.getBeginArrowSize().getValue());
System.out.println(line.getEndArrow().getValue());
System.out.println(line.getEndArrowSize().getValue());
System.out.println(line.getLineColor().getValue());
System.out.println(line.getLinePattern().getValue());
System.out.println(line.getLineWeight().getValue());
System.out.println(line.getRounding().getValue());

{{< /highlight >}}


