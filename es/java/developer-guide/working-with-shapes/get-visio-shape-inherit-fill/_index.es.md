---
title: Obtener Visio Relleno heredado de forma
type: docs
weight: 100
url: /es/java/get-visio-shape-inherit-fill/
description: Esta sección explica cómo obtener el estilo de relleno de la forma visio heredado de su estilo principal y maestro con Aspose.Diagram.
---
### **Recuperar datos de relleno heredados de una forma Visio**
Las formas Visio pueden heredar el estilo principal y la forma maestra. Los desarrolladores pueden obtener los datos de relleno heredados de una forma Visio. La propiedad InheritFill, expuesta por el[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class, contiene los valores de formato de relleno para la forma heredada por el estilo principal y la forma maestra.
#### **Recuperar muestra de programación de datos de llenado heredados**
El siguiente fragmento de código recupera los datos de relleno heredados de la forma. Por favor revise este código de muestra:


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


