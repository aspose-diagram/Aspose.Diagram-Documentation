---
title: Trabajar con capas
type: docs
weight: 130
url: /es/net/working-with-layers/
description: Esta sección explica cómo agregar u obtener información de capa en una forma visio con Aspose.Diagram.
---
## **Configurar objetos de forma con capas en Visio**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) permite configurar objetos de forma con capas en Microsoft Office Visio diagram. Cada forma puede pertenecer a varias capas para que los desarrolladores puedan administrar las formas para satisfacer las necesidades del usuario final. los[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) El objeto de clase ofrece la propiedad LayerMember que permite agregar y eliminar objetos de forma hacia y desde las capas en el dibujo Visio. Los usuarios pueden administrar estas propiedades mediante programación usando Aspose.Diagram API de la siguiente manera:
### **Configurar muestra de programación de objetos de forma**
El siguiente fragmento de código ayuda a agregar, eliminar y mover propiedades de objetos de forma.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Layers();

// Load a source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");

// Iterate through the shapes
foreach (Aspose.Diagram.Shape shape in page.Shapes)
{
    if (shape.Name.ToLower() == "shape1")
    {
        // Add shape1 in first two layers. Here "0;1" are indexes of the layers
        LayerMem layer = shape.LayerMem;
        layer.LayerMember.Value = "0;1";
    }
    else if (shape.Name.ToLower() == "shape2")
    {
        // Remove shape2 from all the layers
        LayerMem layer = shape.LayerMem;
        layer.LayerMember.Value = "";
    }
    else if (shape.Name.ToLower() == "shape3")
    {
        // Add shape3 in first layer. Here "0" is index of the first layer
        LayerMem layer = shape.LayerMem;
        layer.LayerMember.Value = "0";
    }
}
// Save diagram
diagram.Save(dataDir + "ConfigureShapeLayers_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Agregue una nueva capa en el Visio Diagram**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) permite a los desarrolladores agregar nuevas capas para organizar categorías personalizadas de formas y luego asignar formas a esas capas mediante programación. los[LayerCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/layercollection) La clase ofrece el método Add que permite agregar un nuevo[Capa](http://www.aspose.com/api/net/diagram/aspose.diagram/layer) en el dibujo Visio. Los desarrolladores pueden establecer las propiedades de la capa inicializando su objeto de clase.
### **Agregar muestra de programación de capas**
El siguiente fragmento de código ayuda a agregar objetos de capa.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Layers();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// Initialize a new Layer class object
Layer layer = new Layer();
// Set Layer name
layer.Name.Value = "Layer1";
// Set Layer Visibility
layer.Visible.Value = BOOL.True;
// Set the color checkbox of Layer
layer.IsColorChecked = BOOL.True;
// Add Layer to the particular page sheet
page.PageSheet.Layers.Add(layer);

// Get shape by ID
Shape shape = page.Shapes.GetShape(3);
// Assign shape to this new Layer
shape.LayerMem.LayerMember.Value = layer.IX.ToString();
// Save diagram
diagram.Save(dataDir + "AddLayer_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Recuperar todas las capas del Visio Diagram**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) da acceso a los desarrolladores para obtener las capas existentes de un Visio diagram. El[PáginaHoja](http://www.aspose.com/api/net/diagram/aspose.diagram/pagesheet) propiedad de la[Página](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class permite recuperar la lista de capas disponibles de un Visio diagram usando[LayerCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/layercollection) clase.
### **Ejemplo de programación de recuperación de capas**
El siguiente fragmento de código ayuda a obtener la lista de capas.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Layers();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// Iterate through the layers
foreach (Layer layer in page.PageSheet.Layers)
{
    Console.WriteLine("Name: " + layer.Name.Value);
    Console.WriteLine("Visibility: " + layer.Visible.Value);
    Console.WriteLine("Status: " + layer.Status.Value);
}

{{< /highlight >}}

