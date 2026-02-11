---
title: Obtener Visio Forma Heredar caracteres
type: docs
weight: 101
url: /es/net/get-visio-shape-inherit-chars/
description: Esta sección explica cómo obtener el estilo de fuente de la forma visio heredado de su estilo principal y maestro con Aspose.Diagram.
---
### **Recuperar datos de fuente heredados de una forma Visio**
 Las formas Visio pueden heredar el estilo principal y la forma maestra. Los desarrolladores pueden obtener o configurar los datos de fuente heredados de una forma Visio. La propiedad InheritLine, expuesta por el[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class, contiene los valores de formato de línea para la forma heredada por el estilo principal y la forma maestra.
#### **Ejemplo de programación de recuperación de datos de fuente heredados**
El siguiente fragmento de código recupera los datos de fuente heredados de la forma. Por favor revise este código de muestra:


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
	Aspose.Diagram.Char ch = shape.InheritChars.GetChar(0);
	Console.WriteLine(ch.Style.Value);
	Console.WriteLine(ch.Color.Value); 
	Console.WriteLine(ch.FontName.Value); 
	Console.WriteLine(ch.Size.Value);
	Console.WriteLine(ch.Case.Value);
	Console.WriteLine(ch.IsUnderline);
	Console.WriteLine(ch.IsItalic);
	Console.WriteLine(ch.IsStrikethrough);
	Console.WriteLine(ch.IsDoubleStrikethrough);
	Console.WriteLine(ch.IsSubscript);
	Console.WriteLine(ch.IsSuperscript); 
}

{{< /highlight >}}


