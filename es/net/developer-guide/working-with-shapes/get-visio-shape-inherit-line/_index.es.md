---
title: Obtener Visio Forma Heredar línea
type: docs
weight: 100
url: /es/net/get-visio-shape-inherit-line/
description: Esta sección explica cómo obtener el estilo de línea de la forma visio heredado de su estilo principal y maestro con Aspose.Diagram.
---
### **Recuperar datos de línea heredados de una forma Visio**
 Las formas Visio pueden heredar el estilo principal y la forma maestra. Los desarrolladores pueden obtener o configurar los datos de línea heredados de una forma Visio. La propiedad InheritLine, expuesta por el[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class, contiene los valores de formato de línea para la forma heredada por el estilo principal y la forma maestra.
#### **Muestra de programación de recuperación de datos de línea heredados**
El siguiente fragmento de código recupera los datos de línea heredados de la forma. Por favor revise este código de muestra:

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

foreach (Aspose.Diagram.Shape shape in page.Shapes)
{
	Line line = shape.InheritLine;
	Console.WriteLine(line.LinePattern.Value);
	Console.WriteLine(line.LineColor.Value);
	Console.WriteLine(line.BeginArrow.Value);
	Console.WriteLine(line.BeginArrowSize.Value);
	Console.WriteLine(line.EndArrow.Value);
	Console.WriteLine(line.EndArrowSize.Value);
	Console.WriteLine(line.LineWeight.Value);
}

{{< /highlight >}}
```

