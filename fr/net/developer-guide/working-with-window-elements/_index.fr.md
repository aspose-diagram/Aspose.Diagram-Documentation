---
title: Travailler avec des éléments de fenêtre
type: docs
weight: 100
url: /fr/net/working-with-window-elements/
description: Cette section explique obtenir la propriété des éléments de fenêtre dans visio avec Aspose.Diagram.
---
## **Récupérer des éléments de fenêtre à partir du dessin Visio**
 La fenêtre principale de l'application Visio peut contenir n'importe quel fichier Visio ouvert, tout comme les navigateurs Web modernes autorisent plusieurs pages Web à onglets dans une seule fenêtre. Les développeurs peuvent récupérer des objets Window en utilisant[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

 La[FenêtreCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/windowcollection) objet représente une liste de[Fenêtre](http://www.aspose.com/api/net/diagram/aspose.diagram/window)objets disponibles dans le dessin. La propriété Windows, exposée par la classe Diagram, prend en charge une collection d'objets Aspose.Diagram.Window. Cette propriété peut être utilisée pour récupérer les informations de la fenêtre, c'est-à-dire l'ID, le type, la hauteur, la largeur et l'état de la fenêtre.
### **Récupérer l'exemple de programmation des éléments de la fenêtre**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_WindowElements();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Iterate through the window elements
foreach (Window window in diagram.Windows)
{
    Console.WriteLine("ID: " + window.ID);
    Console.WriteLine("Type: " + window.WindowType);
    Console.WriteLine("Window height: " + window.WindowHeight);
    Console.WriteLine("Window width: " + window.WindowWidth);
    Console.WriteLine("Window state: " + window.WindowState);
}

{{< /highlight >}}

## **Ajouter un élément de fenêtre au Visio Diagram**
 La fenêtre principale de l'application Visio peut contenir n'importe quel fichier Visio ouvert, tout comme les navigateurs Web modernes autorisent plusieurs pages Web à onglets dans une seule fenêtre. Les développeurs peuvent désormais ajouter un nouvel objet Window dans une instance Microsoft Visio en utilisant[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

 La[Fenêtre](http://www.aspose.com/api/net/diagram/aspose.diagram/window) L'objet représente une fenêtre ouverte dans une instance Microsoft Visio. La[Ajouter](http://www.aspose.com/api/net/diagram/aspose.diagram/windowcollection/methods/add) méthode, exposée par le[FenêtreCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/windowcollection) class, permet d'ajouter un nouvel objet Window.
### **Ajouter un exemple de programmation d'élément de fenêtre**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_WindowElements();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Initialize window object
Window window = new Window();
// Set window state
window.WindowState = WindowStateValue.Maximized;
// Set window height
window.WindowHeight = 500;
// Set window width
window.WindowWidth = 500;
// Set window type
window.WindowType = WindowTypeValue.Stencil;
// Add window object
diagram.Windows.Add(window);

// Save in any supported format
diagram.Save(dataDir + "AddWindowElementInVisio_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Ajouter la prise en charge des grilles dynamiques et des points de connexion**
La grille dynamique vous aide à positionner de nouvelles formes verticalement et horizontalement par rapport aux formes que vous avez déjà placées dans le dessin. Concernant les points de connexion, une fois marqués comme cochés, cela nous aidera à voir les points de connexion lorsque nous sommes en train de nous y connecter. Nous pouvons réaliser les deux options en utilisant[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).
### **Prise en charge des grilles dynamiques et des points de connexion dans les dessins Visio**
 La[Fenêtre](http://www.aspose.com/api/net/diagram/aspose.diagram/window) La classe offre les propriétés DynamicGridEnabled et ShowConnectionPoints. Ces propriétés peuvent être utilisées pour appliquer des paramètres pour prendre en charge les grilles dynamiques et afficher les options de points de connexion.
#### **Ajouter un exemple de programmation de support**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_WindowElements();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get window object by index
Window window = diagram.Windows[0];
// Check dynamic grid option
window.DynamicGridEnabled = BOOL.True;
// Check connection points option
window.ShowConnectionPoints = BOOL.True;
            
// Save visio drawing
diagram.Save(dataDir + "AddSupportOfVisualAids_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Afficher et masquer les grilles, les règles, les guides et les sauts de page du Visio Diagram**
 Microsoft Office Visio a une paire de règles, une grille et deux types de guides et un indicateur de saut de page pour voir ce qui sera imprimé sur chaque page. Les développeurs peuvent appliquer ces paramètres à l'aide de[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/)Les paramètres s'appliquent globalement à une seule page.

 La[Fenêtre](http://www.aspose.com/api/net/diagram/aspose.diagram/window)La classe offre les propriétés ShowGrid, ShowGuides, ShowRulers et ShowPageBreaks. Ces propriétés peuvent être utilisées pour appliquer des paramètres pour afficher et masquer les grilles, les guides, les règles et les sauts de page.
### **Exemple de programmation**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_WindowElements();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get window object by index
Window window = diagram.Windows[0];
// Set visibility of grid
window.ShowGrid = BOOL.True;
// Set visibility of guides
window.ShowGuides = BOOL.True;
// Set visibility of rulers
window.ShowRulers = BOOL.True;
// Set visibility of page breaks
window.ShowPageBreaks = BOOL.True;

// Save diagram
diagram.Save(dataDir + "DisplayGridsRulersGuidesAndPageBreaks_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

