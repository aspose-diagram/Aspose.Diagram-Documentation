---
title: Arbeiten mit Ebenen
type: docs
weight: 130
url: /de/net/working-with-layers/
description: In diesem Abschnitt wird erläutert, wie Sie Layer-Informationen in einem visio-Shape mit Aspose.Diagram hinzufügen oder abrufen.
---
## **Konfigurieren Sie Formobjekte mit Ebenen in Visio**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) ermöglicht die Konfiguration von Formobjekten mit Ebenen in Microsoft Office Visio diagram. Jede Form kann zu mehreren Ebenen gehören, sodass Entwickler Formen verwalten können, die den Anforderungen des Endbenutzers entsprechen. Das[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Das Klassenobjekt bietet die LayerMember-Eigenschaft, mit der Formobjekte zu den Ebenen in der Visio-Zeichnung hinzugefügt und daraus entfernt werden können. Benutzer können diese Eigenschaften programmgesteuert mit Aspose.Diagram API wie folgt verwalten:
### **Shape Objects Programmierbeispiel konfigurieren**
Der folgende Codeabschnitt hilft beim Hinzufügen, Entfernen und Verschieben von Formobjekteigenschaften.


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

## **Fügen Sie eine neue Ebene in Visio Diagram hinzu**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) ermöglicht es Entwicklern, neue Ebenen hinzuzufügen, um benutzerdefinierte Kategorien von Formen zu organisieren, und diesen Ebenen dann programmgesteuert Formen zuzuweisen. Das[LayerCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/layercollection) Die Klasse bietet die Add-Methode, mit der Sie eine neue hinzufügen können[Schicht](http://www.aspose.com/api/net/diagram/aspose.diagram/layer) in der Zeichnung Visio. Entwickler können Layer-Eigenschaften festlegen, indem sie ihr Klassenobjekt initialisieren.
### **Layer-Programmierbeispiel hinzufügen**
Der folgende Codeabschnitt hilft beim Hinzufügen von Layer-Objekten.


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

## **Rufen Sie alle Ebenen von Visio Diagram ab**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) gibt Entwicklern Zugriff auf die vorhandenen Schichten eines Visio diagram. Die[Seitenblatt](http://www.aspose.com/api/net/diagram/aspose.diagram/pagesheet) Eigentum der[Buchseite](http://www.aspose.com/api/net/diagram/aspose.diagram/page) Klasse ermöglicht das Abrufen der Liste der verfügbaren Layer von einem Visio diagram mit[LayerCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/layercollection) Klasse.
### **Programmierbeispiel für Schichten abrufen**
Der folgende Codeabschnitt hilft beim Abrufen der Liste der Ebenen.


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

