---
title: Cambiar propiedades de capa
type: docs
weight: 130
url: /es/net/change-properties-layer/
description: Esta sección explica cómo cambiar las propiedades de la capa con Aspose.Diagram.
---
## **Cambiar propiedades de capa en Visio**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) permite cambiar las propiedades de la capa en Microsoft Office Visio diagram. Cada forma puede pertenecer a varias capas para que los desarrolladores puedan cambiar las propiedades de la capa para satisfacer las necesidades del usuario final. los[PáginaHoja](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet)El objeto de clase ofrece capas que permiten agregar y eliminar objetos de capa en el dibujo Visio. Los usuarios pueden administrar[Capa](https://reference.aspose.com/diagram/net/aspose.diagram/layer) properties programáticamente usando Aspose.Diagram API de la siguiente manera:
### **Ejemplo de programación de propiedades de capa de cambio**
El siguiente fragmento de código ayuda a cambiar las propiedades de la capa.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Layers();

// Load a source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");

// Iterate through the layers
foreach (Aspose.Diagram.Layer layer in Page.PageSheet.Layers)
{
    layer.Visible.Value = Aspose.Diagram.BOOL.True;
    layer.Print.Value = Aspose.Diagram.BOOL.True;
}
// Save diagram
diagram.Save(dataDir + "ChangeLayerProperty_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```