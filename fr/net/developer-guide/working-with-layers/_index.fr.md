---
title: Travailler avec des calques
type: docs
weight: 130
url: /fr/net/working-with-layers/
description: Cette section explique comment ajouter ou obtenir des informations de calque dans une forme visio avec Aspose.Diagram.
---
## **Configurer des objets de forme avec des calques dans Visio**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) permet de configurer des objets de forme avec des calques dans Microsoft Office Visio diagram. Chaque forme peut appartenir à plusieurs calques afin que les développeurs puissent gérer les formes en fonction des besoins de l'utilisateur final. La[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) L'objet de classe offre la propriété LayerMember qui permet d'ajouter et de supprimer des objets de forme vers et depuis les calques dans le dessin Visio. Les utilisateurs peuvent gérer ces propriétés par programmation en utilisant Aspose.Diagram API comme suit :
### **Configurer l'exemple de programmation d'objets de forme**
Le morceau de code suivant permet d'ajouter, de supprimer et de déplacer des propriétés d'objet de forme.


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

## **Ajouter un nouveau calque dans le Visio Diagram**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) permet aux développeurs d'ajouter de nouveaux calques pour organiser des catégories personnalisées de formes, puis d'attribuer des formes à ces calques par programmation. La[LayerCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/layercollection) la classe propose la méthode Add qui permet d'ajouter un nouveau[Couche](http://www.aspose.com/api/net/diagram/aspose.diagram/layer) dans le dessin Visio. Les développeurs peuvent définir les propriétés de la couche en initialisant son objet de classe.
### **Ajouter un exemple de programmation de couche**
Le morceau de code suivant permet d'ajouter des objets Layer.


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

## **Récupérer toutes les couches du Visio Diagram**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) donne accès aux développeurs pour obtenir les couches existantes d'un Visio diagram. Le[Feuille de page](http://www.aspose.com/api/net/diagram/aspose.diagram/pagesheet) propriété de la[Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class permet de récupérer la liste des couches disponibles à partir d'un Visio diagram en utilisant[LayerCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/layercollection) classer.
### **Récupérer un exemple de programmation de calques**
Le morceau de code suivant aide à obtenir la liste des couches.


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

