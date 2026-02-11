---
title: Travailler avec des hyperliens
type: docs
weight: 110
url: /fr/java/working-with-hyperlinks/
---
## **Ajouter un lien hypertexte à une forme Visio**
C'est une approche facile pour ajouter dynamiquement un lien hypertexte à la forme Microsoft Visio.

Sur les dessins multi-pages Visio, des hyperliens peuvent vous déplacer d'une page à l'autre. Vous pouvez également lier votre dessin à une page Web ou à un fichier sur votre système.

Ces propriétés sont exposées par la[Forme](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) la classe soutient la[com.aspose.diagram.Hyperlink](https://reference.aspose.com/diagram/java/com.aspose.diagram/hyperlink) objet. La méthode add peut être utilisée pour ajouter les données de lien hypertexte d'une forme.

Pour identifier les propriétés dans Microsoft Visio :

1. Dans un diagram, cliquez avec le bouton droit sur une forme.
1.  Sélectionner**Lien hypertexte**.
1. Définir les propriétés existantes
1.  Presse**D'ACCORD** bouton

**Données de lien hypertexte d'une forme, comme dans Microsoft Visio**

![tâche : image_autre_texte](working-with-hyperlinks_1.png)

Les extraits de code ci-dessous ajoutent les données de lien hypertexte de la forme.
### **Ajouter un exemple de programmation de lien hypertexte**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AddHyperlinkToShape.class);   
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");
// get shape by ID
Shape shape = page.getShapes().getShape(2);

//initialize Hyperlink object
Hyperlink hyperlink = new Hyperlink();
//set address value
hyperlink.getAddress().setValue("http://www.google.com/");
//set sub address value
hyperlink.getSubAddress().setValue("Sub address here");
//set description value
hyperlink.getDescription().setValue("Description here");
//set name
hyperlink.setName("MyHyperLink");

//add hyperlink to the shape
shape.getHyperlinks().add(hyperlink);            
//save diagram to local space
diagram.save(dataDir + "AddHyperlinkToShape_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Obtenir les données des liens hypertexte des formes Visio**
 Il est possible d'obtenir les données de lien hypertexte d'une forme de la même manière que vous[lecture des données de forme Visio]().

Les développeurs peuvent récupérer tous les hyperliens d'une forme Visio de la même manière qu'ils[lire les données de forme Visio]() utilisant[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/)

Dans les dessins multipages Visio, les hyperliens peuvent vous déplacer d'une page à l'autre. Vous pouvez également lier votre dessin à une page Web ou à un fichier sur votre système.

Ces propriétés sont exposées par la[Forme](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) la classe soutient la[com.aspose.diagram.Hyperlink](https://reference.aspose.com/diagram/java/com.aspose.diagram/hyperlink)objet. La propriété peut être utilisée pour lire les données de lien hypertexte d'une forme.

Pour identifier les propriétés dans Microsoft Visio :

1. Dans un diagram, cliquez avec le bouton droit sur une forme.
1.  Sélectionner**Lien hypertexte.**
 Toutes les propriétés existantes sont répertoriées dans la boîte de dialogue.

**Données de lien hypertexte d'une forme, comme dans Microsoft Visio**

![tâche : image_autre_texte](working-with-hyperlinks_2.png)

**Une fenêtre de console affichant la sortie des données de forme**

![tâche : image_autre_texte](working-with-hyperlinks_3.png)

Les extraits de code ci-dessous lisent les données de lien hypertexte de la forme.
### **Obtenir un exemple de programmation d'hyperliens**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetHyperlinks.class);  
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");
// get shape by ID
Shape shape = page.getShapes().getShape(1);
// iterate through the hyperlinks
for (Hyperlink hyperlink :(Iterable<Hyperlink>) shape.getHyperlinks())
{
    System.out.println("Address: " + hyperlink.getAddress().getValue());
    System.out.println("Sub Address: " + hyperlink.getSubAddress().getValue());
    System.out.println("Description: " + hyperlink.getDescription().getValue());
}

{{< /highlight >}}
```
