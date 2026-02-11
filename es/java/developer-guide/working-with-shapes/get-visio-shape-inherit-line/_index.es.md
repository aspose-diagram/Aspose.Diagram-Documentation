---
title: Obtener Visio Forma Heredar línea
type: docs
weight: 100
url: /es/java/get-visio-shape-inherit-line/
description: Esta sección explica cómo obtener el estilo de línea de la forma visio heredado de su estilo principal y maestro con Aspose.Diagram.
---
### **Recuperar datos de línea heredados de una forma Visio**
 Las formas Visio pueden heredar el estilo principal y la forma maestra. Los desarrolladores pueden obtener o configurar los datos de línea heredados de una forma Visio. La propiedad InheritLine, expuesta por el[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class, contiene los valores de formato de línea para la forma heredada por el estilo principal y la forma maestra.
#### **Muestra de programación de recuperación de datos de línea heredados**
El siguiente fragmento de código recupera los datos de línea heredados de la forma. Por favor revise este código de muestra:

```
{{< highlight "java" >}}
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
```

