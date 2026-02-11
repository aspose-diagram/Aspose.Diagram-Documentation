---
title: Obtener Visio Relleno heredado de forma
type: docs
weight: 100
url: /es/net/get-visio-shape-inherit-fill/
description: Esta sección explica cómo obtener el estilo de relleno de la forma visio heredado de su estilo principal y maestro con Aspose.Diagram.
---
### **Recuperar datos de relleno heredados de una forma Visio**
Las formas Visio pueden heredar el estilo principal y la forma maestra. Los desarrolladores pueden obtener los datos de relleno heredados de una forma Visio. La propiedad InheritFill, expuesta por el[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class, contiene los valores de formato de relleno para la forma heredada por el estilo principal y la forma maestra.
#### **Recuperar muestra de programación de datos de llenado heredados**
El siguiente fragmento de código recupera los datos de relleno heredados de la forma. Por favor revise este código de muestra:


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

foreach (Aspose.Diagram.Shape shape in page.Shapes)
{
	Fill f = shape.InheritFill;
	Console.WriteLine(f.FillForegnd.Value);
	Console.WriteLine(f.FillPattern.Value);
	Console.WriteLine(f.ShdwForegnd.Value);
	Console.WriteLine(f.ShdwPattern.Value);
}

{{< /highlight >}}


