---
title: Récupérer les connecteurs Visio et les informations sur la police
type: docs
weight: 20
url: /fr/java/retrieve-visio-connectors-and-font-information/
---
## **Récupération des informations sur le connecteur**
 Aspose.Diagram for Java fournit des mécanismes pour récupérer des informations - ID et nom - sur[pages](/diagram/fr/java/retrieve-get-copy-and-insert-a-page/) et[Maître](). Il vous permet également d'obtenir des informations sur les connecteurs, les éléments qui relient les formes.

 La[Relier](https://reference.aspose.com/diagram/java/com.aspose.diagram/connect) L'objet représente un connecteur qui relie deux formes sur une page de dessin Visio. La propriété Connects, exposée par la[Page](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) prend en charge une collection d'objets Aspose.Diagram.Connect. Cette propriété peut être utilisée pour récupérer des informations d'ID et de nom sur un connecteur.

**Une fenêtre de console affichant la sortie du code ci-dessous.** 

![tâche : image_autre_texte](retrieve-visio-connectors-and-font-information_1.png)
### **Exemple de programmation**
Le morceau de code suivant récupère les informations pour les connecteurs dans un diagram.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RetrieveConnectorInfo.class);
        
//Call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "RetrieveConnectorInfo.vsd");        
for(Connect connector : (Iterable<Connect>) diagram.getPages().getPage(0).getConnects())
{
    // Display information about the Connectors
    System.out.println("\nFrom Shape ID : " + connector.getFromSheet());
    System.out.println("To Shape ID : " + connector.getToSheet());
 }

System.out.println("Process Completed Successfully");

{{< /highlight >}}
```
## **Récupération des informations sur la police**
 Aspose.Diagram a des mécanismes pour récupérer des informations sur les éléments qui composent un diagram, à partir de[pages](/diagram/fr/java/retrieve-get-copy-and-insert-a-page/), [pochoirs](), [connecteurs](https://reference.aspose.com/diagram/java/com.aspose.diagram/ConnectCollection)et aussi les polices. Cet article montre comment savoir quelles polices sont utilisées dans un diagram.

 La[Police de caractère](https://reference.aspose.com/diagram/java/com.aspose.diagram/font) L'objet représente une police de caractères qui est soit appliquée au texte d'un document, soit disponible pour une utilisation sur le système.

Un objet Font mappe un nom (par exemple, « Arial ») à l'ID de police (par exemple, 3) que Microsoft Visio stocke dans une cellule Police d'une section Caractère d'une forme qui contient du texte mis en forme avec cette police. Les ID de police peuvent changer lorsqu'un document est ouvert sur différents systèmes ou lorsque des polices sont installées ou supprimées.
### **Récupération d'un exemple de programmation de polices**
Le morceau de code suivant récupère les informations de police du Visio diagram.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RetrieveFontInfo.class);

// call the diagram constructor to load diagram
Diagram diagram = new Diagram(dataDir+ "RetrieveFontInfo.vsd");

for(Font font : (Iterable<Font>) diagram.getFonts())
{
    // Display information about the fonts
    System.out.println(font.getName());
}

System.out.println("Process Completed Successfully");

{{< /highlight >}}
```

![tâche : image_autre_texte](retrieve-visio-connectors-and-font-information_2.png)
### **Obtenir le répertoire de polices par défaut**
Aspose.Diagram for Java API permet également d'obtenir le chemin du répertoire de polices par défaut à l'aide de la méthode getDefaultFontDir() de la classe Diagram. Le morceau de code suivant récupère le répertoire de polices par défaut à partir du Visio diagram.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveFontInfo.class) + "Diagrams/";

// Call the diagram constructor to load diagram
Diagram diagram = new Diagram(dataDir + "RetrieveFontInfo.vsd");

// Display font default directory
System.out.println(diagram.getDefaultFontDir());

{{< /highlight >}}
```
