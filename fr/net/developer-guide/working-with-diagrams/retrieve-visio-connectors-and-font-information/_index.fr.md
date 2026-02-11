---
title: Récupérer les connecteurs Visio et les informations sur la police
type: docs
weight: 20
url: /fr/net/retrieve-visio-connectors-and-font-information/
description: Cette section explique comment obtenir les connecteurs visio et les informations sur les polices.
---
## **Récupération des informations sur le connecteur**
 Aspose.Diagram for .NET fournit des mécanismes pour récupérer des informations - ID et nom - sur[pages](/diagram/fr/net/retrieve-2c-get-2c-copy-and-insert-a-page/) et[Maître](https://docs.aspose.com/diagram/net/working-with-masters/). Il vous permet également d'obtenir des informations sur les connecteurs, les éléments qui relient les formes.

 La[Relier](http://www.aspose.com/api/net/diagram/aspose.diagram/connect) L'objet représente un connecteur qui relie deux formes sur une page de dessin Visio. La propriété Connects, exposée par la[Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page) prend en charge une collection d'objets Aspose.Diagram.Connect. Cette propriété peut être utilisée pour récupérer des informations d'ID et de nom sur un connecteur.
### **Exemple de programmation**
Le morceau de code suivant récupère les informations pour les connecteurs dans un diagram.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Call the diagram constructor to load diagram from a VSD file
Diagram vdxDiagram = new Diagram(dataDir + "RetrieveConnectorInfo.vsd");

foreach (Aspose.Diagram.Connect connector in vdxDiagram.Pages[0].Connects)
{
    // Display information about the Connectors
    Console.WriteLine("\nFrom Shape ID : " + connector.FromSheet);
    Console.WriteLine("To Shape ID : " + connector.ToSheet);
}

{{< /highlight >}}
```
## **Récupération des informations sur la police**
 Aspose.Diagram a des mécanismes pour récupérer des informations sur les éléments qui composent un diagram, à partir de[pages](/diagram/fr/net/retrieve-2c-get-2c-copy-and-insert-a-page/), [pochoirs](https://docs.aspose.com/diagram/net/working-with-masters/), [connecteurs](/diagram/fr/net/retrieving-connector-information/)et aussi les polices. Cet article montre comment savoir quelles polices sont utilisées dans un diagram.

 La[Police de caractère](http://www.aspose.com/api/net/diagram/aspose.diagram/font) L'objet représente une police de caractères qui est soit appliquée au texte d'un document, soit disponible pour une utilisation sur le système. Un objet Font mappe un nom (par exemple, « Arial ») à l'ID de police (par exemple, 3) que Microsoft Visio stocke dans une cellule Police d'une section Caractère d'une forme qui contient du texte mis en forme avec cette police. Les ID de police peuvent changer lorsqu'un document est ouvert sur différents systèmes ou lorsque des polices sont installées ou supprimées.
### **Récupération d'un exemple de programmation de polices**
Le morceau de code suivant récupère les informations de police du Visio diagram.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Call the diagram constructor to load diagram from a VSD file
Diagram vdxDiagram = new Diagram(dataDir + "RetrieveFontInfo.vsd");

foreach (Aspose.Diagram.Font font in vdxDiagram.Fonts)
{
    // Display information about the fonts
    Console.WriteLine(font.Name);
}

{{< /highlight >}}
```
### **Obtenir le répertoire de polices par défaut**
Aspose.Diagram for .NET API permet également d'obtenir le chemin du répertoire de polices par défaut à l'aide de la méthode GetDefaultFontDir() de la classe Diagram. Le morceau de code suivant récupère le répertoire de polices par défaut à partir du Visio diagram.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Call the diagram constructor to load diagram from a VSD file
Diagram vdxDiagram = new Diagram(dataDir + "RetrieveFontInfo.vsd");
           
// Display font default directory
Console.WriteLine(vdxDiagram.GetDefaultFontDir());

{{< /highlight >}}
```
### **Obtenir des polices inutilisées**
{{% alert color="primary" %}}

Cette méthode est prise en charge par la version 19.6 ou supérieure.

{{% /alert %}}

Aspose.Diagram for .NET API permet également d'obtenir des polices inutilisées à l'aide de la méthode GetUnusedStyles() de la classe Diagram. Le morceau de code suivant récupère les polices inutilisées du Visio diagram.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Call the diagram constructor to load diagram from a VSD file
Diagram vdxDiagram = new Diagram(dataDir + "Sample_UnusedFonts.vsdx");

// Get Unused Fonts 
StyleSheetCollection unused = vdxDiagram.GetUnusedStyles();

// Display unused fonts count 
Console.WriteLine(unused.Count);

{{< /highlight >}}
```
