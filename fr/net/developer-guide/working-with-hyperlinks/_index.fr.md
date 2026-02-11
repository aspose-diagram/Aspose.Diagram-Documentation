---
title: Travailler avec des hyperliens
type: docs
weight: 160
url: /fr/net/working-with-hyperlinks/
description: Cette section explique comment ajouter ou obtenir un lien hypertexte dans une forme Visio avec Aspose.Diagram.
---
## **Ajouter un lien hypertexte à une forme Visio**
Microsoft Office Visio prend en charge l'ajout de liens hypertexte à n'importe quelle forme. Les liens hypertexte peuvent pointer vers une autre page ou forme du dessin courant, une page ou forme d'un autre dessin, un document autre qu'un dessin Visio, un site Web, un site FTP ou une adresse de messagerie. Les développeurs peuvent utiliser Aspose.Diagram API pour ajouter facilement des liens hypertexte à une forme Visio.

 Dans le dessin multi-pages Visio, les hyperliens peuvent vous faire naviguer d'une forme à de nombreux autres types de liens.[Collection de liens hypertexte](http://www.aspose.com/api/net/diagram/aspose.diagram/hyperlinkcollection) exposé par le[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) La classe propose la méthode Add qui peut être utilisée pour ajouter le lien hypertexte d'une forme.

Pour identifier les propriétés au Microsoft Office Visio :

1. Dans un Visio diagram, cliquez avec le bouton droit sur une forme.
1.  Sélectionner**Lien hypertexte.**
1. Définir les propriétés existantes
1.  Presse**D'ACCORD** bouton

**Données de lien hypertexte d'une forme, comme dans Microsoft Visio**

![tâche : image_autre_texte](working-with-hyperlinks_1.png)
### **Ajouter un exemple de programmation de lien hypertexte**
L'extrait de code ci-dessous ajoute les données de lien hypertexte de la forme.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Hyperlinks();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");
// Get shape by ID
Shape shape = page.Shapes.GetShape(2);

// Initialize Hyperlink object
Hyperlink hyperlink = new Hyperlink();
// Set address value
hyperlink.Address.Value = "http:// Www.google.com/";
// Set sub address value
hyperlink.SubAddress.Value = "Sub address here";
// Set description value
hyperlink.Description.Value = "Description here";
// Set name
hyperlink.Name = "MyHyperLink";

// Add hyperlink to the shape
shape.Hyperlinks.Add(hyperlink);            
// Save diagram to local space
diagram.Save(dataDir + "AddHyperlinkToShape_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Obtenir les données des liens hypertexte des formes Visio**
Les développeurs peuvent récupérer tous les hyperliens d'une forme Visio de la même manière qu'ils[lire les données de forme Visio](https://docs.aspose.com/diagram/net/load-or-create-a-visio-drawing/) utilisant[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

Dans le dessin multi-pages Visio, les hyperliens peuvent vous faire naviguer d'une forme à de nombreux autres types de liens.[Collection de liens hypertexte](http://www.aspose.com/api/net/diagram/aspose.diagram/hyperlinkcollection) exposé par le[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) permet aux développeurs de récupérer des hyperliens.

Pour identifier les propriétés au Microsoft Office Visio :

1. Dans un diagram, cliquez avec le bouton droit sur une forme.
1.  Sélectionner**Lien hypertexte.**

Toutes les propriétés existantes sont répertoriées dans la boîte de dialogue.
**Données de lien hypertexte d'une forme, comme dans Microsoft Visio**

![tâche : image_autre_texte](working-with-hyperlinks_1.png)

**Une fenêtre de console affichant la sortie des données de forme**

![tâche : image_autre_texte](working-with-hyperlinks_3.png)
### **Obtenir un exemple de programmation d'hyperliens**
L'extrait de code ci-dessous lit les données du lien hypertexte de la forme.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Hyperlinks();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");
// Get shape by ID
Shape shape = page.Shapes.GetShape(1);
// Iterate through the hyperlinks
foreach (Aspose.Diagram.Hyperlink hyperlink in shape.Hyperlinks)
{
    Console.WriteLine("Address: " + hyperlink.Address.Value);
    Console.WriteLine("Sub Address: " + hyperlink.SubAddress.Value);
    Console.WriteLine("Description: " + hyperlink.Description.Value);
}       

{{< /highlight >}}
```
