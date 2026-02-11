---
title: Travailler avec des éléments de fenêtre
type: docs
weight: 130
url: /fr/java/working-with-window-elements/
---
## **Récupérer des éléments de fenêtre à partir du dessin Visio**
 La fenêtre principale de l'application Visio peut contenir n'importe quel fichier Visio ouvert, tout comme les navigateurs Web modernes autorisent plusieurs pages Web à onglets dans une seule fenêtre. Les développeurs peuvent récupérer des objets Window en utilisant[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

 La[FenêtreCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/windowcollection) objet représente une liste de[Fenêtre](https://reference.aspose.com/diagram/java/com.aspose.diagram/window)objets disponibles dans le dessin. La propriété Windows, exposée par la classe Diagram, prend en charge une collection d'objets Aspose.Diagram.Window. Cette propriété peut être utilisée pour récupérer les informations de la fenêtre, c'est-à-dire l'ID, le type, la hauteur, la largeur et l'état de la fenêtre.

**Une fenêtre de console affichant la sortie du code.**

![tâche : image_autre_texte](http://i.imgur.com/zduARGh.png)
### **Récupérer l'exemple de programmation des éléments de la fenêtre**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RetrieveWindowElementsOfDiagram.class);    
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// iterate through the window elements
for (Window window :(Iterable<Window>) diagram.getWindows())
{
    System.out.println("ID: " + window.getID());
    System.out.println("Type: " + window.getWindowType());
    System.out.println("Window height: " + window.getWindowHeight());
    System.out.println("Window width: " + window.getWindowWidth());
    System.out.println("Window state: " + window.getWindowState());
}

{{< /highlight >}}
```
## **Ajouter un élément de fenêtre au Visio Diagram**
 La fenêtre principale de l'application Visio peut contenir n'importe quel fichier Visio ouvert, tout comme les navigateurs Web modernes autorisent plusieurs pages Web à onglets dans une seule fenêtre. Les développeurs peuvent désormais ajouter un nouvel objet Window dans une instance Microsoft Visio en utilisant[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

L'objet Window représente une fenêtre ouverte dans une instance Microsoft Visio. La méthode Add, exposée par la classe WindowCollection, permet d'ajouter un nouvel objet Window.
### **Ajouter un exemple de programmation d'élément de fenêtre**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AddWindowElementInVisio.class); 
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// initialize window object
Window window = new Window();
// set window state
window.setWindowState(WindowStateValue.MAXIMIZED);
// set window height
window.setWindowHeight(500);
// set window width
window.setWindowWidth(500);
// set window type
window.setWindowType(WindowTypeValue.STENCIL);
// add window object
diagram.getWindows().add(window);

// save in any supported format
diagram.save(dataDir + "AddWindowElementInVisio_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Ajouter la prise en charge des grilles dynamiques et des points de connexion**
La grille dynamique vous aide à positionner de nouvelles formes verticalement et horizontalement par rapport aux formes que vous avez déjà placées dans le dessin. Concernant les points de connexion, une fois marqués comme cochés, cela nous aidera à voir les points de connexion lorsque nous sommes en train de nous y connecter. Nous pouvons réaliser les deux options en utilisant[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).
### **Prise en charge des grilles dynamiques et des points de connexion dans les dessins Visio**
La classe Window propose les propriétés DynamicGridEnabled et ShowConnectionPoints. Ces propriétés peuvent être utilisées pour appliquer des paramètres pour prendre en charge les grilles dynamiques et afficher les options de points de connexion.

**Une application Visio montrant les options en Visio.**

![tâche : image_autre_texte](http://i.imgur.com/bxsJIwF.png)
#### **Ajouter un exemple de programmation de support**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AddSupportOfVisualAids.class);
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get window object by index
Window window = diagram.getWindows().get(0);
// check dynamic grid option
window.setDynamicGridEnabled(BOOL.TRUE);
// check connection points option
window.setShowConnectionPoints(BOOL.TRUE);
        
// save visio drawing
diagram.save(dataDir + "AddSupportOfVisualAids_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Afficher et masquer les grilles, les règles, les guides et les sauts de page du Visio Diagram**
 Microsoft Office Visio a une paire de règles, une grille et deux types de guides et un indicateur de saut de page pour voir ce qui sera imprimé sur chaque page. Les développeurs peuvent appliquer ces paramètres à l'aide de[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/)Les paramètres s'appliquent globalement à une seule page.

La classe Window offre les propriétés ShowGrid, ShowGuides, ShowRulers et ShowPageBreaks. Ces propriétés peuvent être utilisées pour appliquer des paramètres pour afficher et masquer les grilles, les guides, les règles et les sauts de page.

**Une application Visio montrant les options en Visio.**

![tâche : image_autre_texte](http://i.imgur.com/E0pvXbP.png)
### **Exemple de programmation**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(DisplayGridsRulersGuidesAndPageBreaks.class);     
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get window object by index
Window window = diagram.getWindows().get(0);
// set visibility of grid
window.setShowGrid(BOOL.TRUE);
// set visibility of guides
window.setShowGuides(BOOL.TRUE);
// set visibility of rulers
window.setShowRulers(BOOL.TRUE);
// set visibility of page breaks
window.setShowPageBreaks(BOOL.TRUE);

// save diagram
diagram.save(dataDir + "DisplayGridsRulersGuidesAndPageBreaks_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
