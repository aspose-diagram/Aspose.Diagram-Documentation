---
title: Visio Şekil Devralma Dolgusunu Alın
type: docs
weight: 100
url: /tr/java/get-visio-shape-inherit-fill/
description: Bu bölüm, visio şeklinin ana stilinden ve Aspose.Diagram ana stilinden devralınan dolgu stilinin nasıl alınacağını açıklar.
---
### **Visio Şeklinin Miras Alınan Dolgu Verilerini Alma**
Visio şekilleri, ana stili ve ana şekli devralabilir. Geliştiriciler, bir Visio şeklinin devralınan Dolgu verilerini alabilir. Tarafından sunulan InheritFill özelliği[Şekil](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class, ana stil ve ana şekil tarafından devralınan şeklin dolgu biçimlendirme değerlerini içerir.
#### **Devralınan Doldurma Verilerini Al Programlama Örneği**
Aşağıdaki kod parçacığı, şeklin devralınan dolgu verilerini alır. Lütfen bu örnek kodu kontrol edin:


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveInheritedFillData.class) + "Shapes/";

// Call the diagram constructor to load a VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get page by ID
Page page = diagram.getPages().getPage("Page-1");
// Get shape by ID
Shape shape = page.getShapes().getShape(1);
// Get the fill formatting values
System.out.println(shape.getInheritFill().getFillBkgnd().getValue());
System.out.println(shape.getInheritFill().getFillForegnd().getValue());
System.out.println(shape.getInheritFill().getFillPattern().getValue());
System.out.println(shape.getInheritFill().getShapeShdwObliqueAngle().getValue());
System.out.println(shape.getInheritFill().getShapeShdwOffsetX().getValue());
System.out.println(shape.getInheritFill().getShapeShdwOffsetY().getValue());
System.out.println(shape.getInheritFill().getShapeShdwScaleFactor().getValue());
System.out.println(shape.getInheritFill().getShapeShdwType().getValue());
System.out.println(shape.getInheritFill().getShdwBkgnd().getValue());
System.out.println(shape.getInheritFill().getShdwBkgndTrans().getValue());
System.out.println(shape.getInheritFill().getShdwForegnd().getValue());
System.out.println(shape.getInheritFill().getShdwForegndTrans().getValue());
System.out.println(shape.getInheritFill().getShdwPattern().getValue());

{{< /highlight >}}


