---
title: Grouper, convertir et vérifier des formes
type: docs
weight: 80
url: /fr/net/group-convert-and-verify-shapes/
description: Cette section explique comment grouper des formes avec Aspose.Diagram.
---
## **Regrouper plusieurs formes dans le dessin Visio**
Aspose.Diagram API permet aux développeurs de regrouper des formes pour les déplacer toutes en même temps. Chaque forme d'un groupe conserve une identité unique et possède son propre ensemble de propriétés. Lorsque nous modifions la mise en forme d'un groupe de formes, il attribue la nouvelle propriété à chaque forme.
### **Comment grouper des formes**
 La méthode Groupe exposée par le[ShapeCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/shapecollection) class peut être utilisé pour regrouper des formes.

Le code ci-dessous montre comment :

1. Charger un échantillon diagram.
1. initialisé un tableau des formes
1. obtenir une forme particulière par identifiant.
1. obtenir une autre forme particulière particulière par identifiant.
1. affecter des formes au tableau.
1. groupez des formes en appelant la méthode Group.
1. enregistrer diagram
#### **Exemple de programmation de formes de groupe**
Utilisez le code suivant dans votre application .NET pour regrouper les formes en utilisant Aspose.Diagram for .NET API.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

// Initialize an array of shapes
Aspose.Diagram.Shape[] ss = new Aspose.Diagram.Shape[3];

// Extract and assign shapes to the array
ss[0] = page.Shapes.GetShape(15);
ss[1] = page.Shapes.GetShape(16);
ss[2] = page.Shapes.GetShape(17);

// Mark array shapes as group
page.Shapes.Group(ss);

// Save visio diagram
diagram.Save(dataDir + "GroupShapes_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Convertir une forme Visio en d'autres formats de fichier**
Aspose.Diagram for .NET API permet aux développeurs de convertir une seule forme Visio en tout autre format de fichier pris en charge. Dans cet article, nous supprimons toutes les autres formes Visio de la page et personnalisons le paramètre de page en fonction de la taille de la forme source.
### **Conversion d'une forme particulière Visio**
Developers can convert a Visio shape to PDF, HTML, Image, SVG, and SWF by **spécifiant les options de sauvegarde Visio**.
Cet exemple de code fonctionne comme suit :

1. Charger une source Visio.
1. Obtenir une page particulière.
1. Supprimez la page d'arrière-plan.
1. Construisez une table de hachage de toutes les formes contenant les identifiants et les noms.
1. Itérer dans la table de hachage
1. Supprimez toutes les formes de la page Visio, sauf celle en particulier.
1. Définissez la taille de la page.
1. Enregistrez la page Visio dans n'importe quel format de fichier pris en charge.
#### **Exemple de programmation de conversion de forme**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram srcVisio = new Diagram(dataDir + "Drawing1.vsdx");

double shapeWidth = 0;
double shapeHeight = 0;

// Get Visio page
Aspose.Diagram.Page srcPage = srcVisio.Pages.GetPage("Page-3");
// Remove background page
srcPage.BackPage = null;

// Get hash table of shapes, it holds id and name
Hashtable remShapes = new Hashtable();
// Hashtable<Long, String> remShapes = new Hashtable<Long, String>();
foreach (Aspose.Diagram.Shape shape in srcPage.Shapes)
    // For the normal shape
    remShapes.Add(shape.ID, shape.Name);

// Iterate through the hash table
foreach (DictionaryEntry shapeEntry in remShapes)
{
    long key = (long)shapeEntry.Key;
    string val = (string)shapeEntry.Value;
    Aspose.Diagram.Shape shape = srcPage.Shapes.GetShape(key);
    // Check of the shape name
    if (val.Equals("GroupShape1"))
    {
        // Move shape to the origin corner
        shapeWidth = shape.XForm.Width.Value;
        shapeHeight = shape.XForm.Height.Value;
        shape.MoveTo(shapeWidth * 0.5, shapeHeight * 0.5);
        // Trim page size
        srcPage.PageSheet.PageProps.PageWidth.Value = shapeWidth;
        srcPage.PageSheet.PageProps.PageHeight.Value = shapeHeight;
    }
    else
    {
        // Remove shape from the Visio page and hash table
        srcPage.Shapes.Remove(shape);
    }
}
remShapes.Clear();

// Specify saving options
Aspose.Diagram.Saving.PdfSaveOptions opts = new Aspose.Diagram.Saving.PdfSaveOptions();
// Set page count to save
opts.PageCount = 1;
// Set starting index of the page
opts.PageIndex = 1;
// Save it
srcVisio.Save(dataDir + "SaveVisioShapeInOtherFormats_out.pdf", opts);

{{< /highlight >}}

### **Convert Visio Shape to PDF**
The ToPdf method of the Shape class allows to convert a shape into the PDF format.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// save a shape in the PDF format

diagram.Pages[0].Shapes.GetShape(59).ToPdf(dataDir + "out.pdf");

{{< /highlight >}}
### **Convert Visio Shape to HTML**
The ToHTML method of the Shape class allows to convert a shape into the HTML format.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Aspose.Diagram.Saving.HTMLSaveOptions hs = new Aspose.Diagram.Saving.HTMLSaveOptions();

// save a shape in the PDF format

diagram.Pages[0].Shapes.GetShape(59).ToHTML(dataDir + "out.pdf", hs);

{{< /highlight >}}
## **Vérifiez si deux formes Visio sont connectées ou collées**
 Aspose.Diagram for .NET API permet aux développeurs de vérifier que les deux formes Visio sont collées ou connectées. Auparavant, nous avons vu comment connecter ou coller deux formes dans ces rubriques d'aide :[Ajouter et connecter des formes Visio](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/) et[Formes de colle à l'intérieur du conteneur](/diagram/fr/net/working-with-shapes-gluing/).
### **Vérification des formes connectées ou collées**
 La[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) La classe offre les propriétés IsGlued et IsConnected pour déterminer si deux formes sont collées ou connectées.
#### **Exemple de programmation de vérification de formes connectées ou collées**
Le morceau de code suivant vérifie si deux formes sont connectées ou collées.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Set two shape ids
long ShapeIdOne = 15;
long ShapeIdTwo = 16;

// Get Visio page by name
Page page = diagram.Pages.GetPage("Page-3");

// Get Visio shapes by ids
Shape ShapedOne = page.Shapes.GetShape(ShapeIdOne);
Shape ShapedTwo = page.Shapes.GetShape(ShapeIdTwo);

// Determine whether shapes are connected
bool connected = ShapedOne.IsConnected(ShapedTwo);
Console.WriteLine("Shapes are connected: " + connected);

// Determine whether shapes are glued
bool glued = ShapedOne.IsGlued(ShapedTwo);
Console.WriteLine("Shapes are Glued: " + glued);

{{< /highlight >}}

## **Vérifiez si la forme Visio se trouve dans un groupe de formes**
Aspose.Diagram for .NET API permet aux développeurs de vérifier que la forme Visio est dans un groupe de formes ou non.
### **Vérification de la forme dans le groupe de formes**
La[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)La classe offre des propriétés IsInGroup pour déterminer si la forme Visio est dans une forme de groupe.
#### **Vérification de la forme dans l'exemple de programmation du groupe de formes**
Le morceau de code suivant vérifie si la forme est dans une forme de groupe.


{{< highlight csharp >}}
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();
// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a sub-shape by page name, group shape ID, and then sub-shape ID
Shape shape = diagram.Pages.GetPage("Page-3").Shapes.GetShape(13).Shapes.GetShape(2);
Console.WriteLine("Is it in a Group: " + shape.IsInGroup());
{{< /highlight >}}

