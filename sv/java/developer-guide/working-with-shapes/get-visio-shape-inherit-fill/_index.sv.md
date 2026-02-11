---
title: Skaffa Visio Shape Inherit Fill
type: docs
weight: 100
url: /sv/java/get-visio-shape-inherit-fill/
description: Det här avsnittet förklarar hur du får visio-formens fyllningsstil ärvd från dess överordnade stil och master med Aspose.Diagram.
---
### **Hämta ärvd fyllningsdata för en Visio-form**
Visio-formerna kan ärva den överordnade stilen och huvudformen. Utvecklare kan få ärvde Fill-data för en Visio-form. Egenskapen InheritFill, exponerad av[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) klass, innehåller fyllningsformateringsvärdena för formen som ärvs av den överordnade stilen och huvudformen.
#### **Hämta ärvt fyllningsdataprogrammeringsexempel**
Följande kodavsnitt hämtar formens ärvda fyllningsdata. Kontrollera denna exempelkod:


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


