---
title: Arbeta med lager
type: docs
weight: 130
url: /sv/net/working-with-layers/
description: Det här avsnittet förklarar hur du lägger till eller får lagerinformation i en visio-form med Aspose.Diagram.
---
## **Konfigurera Shape-objekt med lager i Visio**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) gör det möjligt att konfigurera formobjekt med lager i Microsoft Office Visio diagram. Varje form kan tillhöra flera lager så att utvecklare kan hantera former för att passa slutanvändarens behov. De[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class object erbjuder LayerMember-egenskapen som gör det möjligt att lägga till och ta bort formobjekt till och från lagren i Visio-ritningen. Användare kan hantera dessa egenskaper programmatiskt med Aspose.Diagram API enligt följande:
### **Konfigurera formobjekts programmeringsexempel**
Följande kodbit hjälper till att lägga till, ta bort och flytta formobjektegenskaper.

```
{{< highlight "csharp" >}}
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
```
## **Lägg till ett nytt lager i Visio Diagram**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) tillåter utvecklare att lägga till nya lager för att organisera anpassade kategorier av former och sedan tilldela former till dessa lager programmatiskt. De[LayerCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/layercollection) klass erbjuder Lägg till metod som gör det möjligt att lägga till en ny[Lager](http://www.aspose.com/api/net/diagram/aspose.diagram/layer) i Visio-ritningen. Utvecklare kan ställa in lageregenskaper genom att initiera dess klassobjekt.
### **Lägg till lagerprogrammeringsexempel**
Följande kodbit hjälper till att lägga till Layer-objekt.

```
{{< highlight "csharp" >}}
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
```
## **Hämta alla lager från Visio Diagram**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) ger tillgång till utvecklare att få de befintliga lagren av en Visio diagram.[PageSheet](http://www.aspose.com/api/net/diagram/aspose.diagram/pagesheet) egendom av[Sida](http://www.aspose.com/api/net/diagram/aspose.diagram/page) klass gör det möjligt att hämta listan över tillgängliga lager från en Visio diagram med[LayerCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/layercollection) klass.
### **Hämta lagerprogrammeringsexempel**
Följande kodbit hjälper dig att få listan över lager.

```
{{< highlight "csharp" >}}
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
```
