---
title: Lavorare con i livelli
type: docs
weight: 130
url: /it/net/working-with-layers/
description: Questa sezione spiega come aggiungere o ottenere informazioni sui layer in una forma visio con Aspose.Diagram.
---
## **Configura gli oggetti forma con i livelli in Visio**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) consente di configurare oggetti forma con livelli in Microsoft Office Visio diagram. Ogni forma può appartenere a più livelli in modo che gli sviluppatori possano gestire le forme in base alle esigenze dell'utente finale. Il[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) L'oggetto class offre la proprietà LayerMember che consente di aggiungere e rimuovere oggetti forma da e verso i livelli nel disegno Visio. Gli utenti possono gestire queste proprietà a livello di codice utilizzando Aspose.Diagram API come segue:
### **Configurare l'esempio di programmazione degli oggetti Shape**
Il seguente pezzo di codice aiuta ad aggiungere, rimuovere e spostare le proprietà dell'oggetto forma.


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

## **Aggiungi un nuovo livello nel Visio Diagram**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) consente agli sviluppatori di aggiungere nuovi livelli per organizzare categorie personalizzate di forme e quindi assegnare forme a tali livelli in modo programmatico. Il[Raccolta livelli](http://www.aspose.com/api/net/diagram/aspose.diagram/layercollection) class offre il metodo Add che consente di aggiungere un nuovo[Strato](http://www.aspose.com/api/net/diagram/aspose.diagram/layer) nel disegno Visio. Gli sviluppatori possono impostare le proprietà del livello inizializzando il suo oggetto di classe.
### **Aggiungi un esempio di programmazione a livelli**
Il seguente pezzo di codice aiuta ad aggiungere oggetti Layer.


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

## **Recupera tutti i livelli dal Visio Diagram**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) dà accesso agli sviluppatori per ottenere i livelli esistenti di un Visio diagram. Il[PaginaFoglio](http://www.aspose.com/api/net/diagram/aspose.diagram/pagesheet) proprietà del[Pagina](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class consente di recuperare l'elenco dei livelli disponibili da un Visio diagram utilizzando[Raccolta livelli](http://www.aspose.com/api/net/diagram/aspose.diagram/layercollection) classe.
### **Recupera l'esempio di programmazione dei livelli**
Il seguente pezzo di codice aiuta a ottenere l'elenco dei livelli.


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

