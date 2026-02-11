---
title: Gérer les propriétés du document
linktitle: Propriétés du document
type: docs
weight: 80
url: /fr/net/document-properties/
description: Gérer les propriétés de document des fichiers visio.
---
## **Introduction**

Microsoft Visio offre la possibilité d'ajouter des propriétés aux fichiers visio. Ces propriétés de document fournissent des informations utiles et sont divisées en 2 catégories comme détaillé ci-dessous.

- Propriétés définies par le système (intégrées) : les propriétés intégrées contiennent des informations générales sur le document telles que le titre du document, le nom de l'auteur, les statistiques du document, etc.
- Propriétés définies par l'utilisateur (personnalisées) : propriétés personnalisées définies par l'utilisateur final sous la forme d'une paire nom-valeur.

{{% alert color="primary" %}}

Le point le plus important à savoir sur les propriétés intégrées et personnalisées est que les propriétés intégrées peuvent être consultées et modifiées, mais pas créées ou supprimées. Cependant, des propriétés personnalisées peuvent être créées et gérées.

{{% /alert %}}

## **Gestion des propriétés du document à l'aide de Microsoft Visio**

 Microsoft Visio vous permet de gérer les propriétés de document des fichiers Visio de manière WYSIWYG. Veuillez suivre les étapes ci-dessous pour ouvrir le**Propriétés** dialogue au Visio 2016.

1.  Du**Dossier** menu, sélectionnez**Info**.

|**Sélection du menu d'informations**|
|:- |
|![tâche : image_autre_texte](managing-document-properties_1.png)|
1.  Cliquer sur**Propriétés** rubrique et sélectionnez "Propriétés avancées".

|**Cliquer sur la sélection des propriétés avancées**|
|:- |
|![tâche : image_autre_texte](managing-document-properties_2.png)|
1. Gérer les propriétés de document du fichier.

|**Boîte de dialogue Propriétés**|
|:- |
|![tâche : image_autre_texte](managing-document-properties_3.png)|
Dans la boîte de dialogue Propriétés, il existe différents onglets, tels que Général, Résumé, Statistiques, Contenu et Personnalisés. Chaque onglet permet de configurer différents types d'informations relatives au fichier. L'onglet Personnalisé est utilisé pour gérer les propriétés personnalisées.

## **Utilisation des propriétés du document à l'aide de Aspose.Diagram**

Les développeurs peuvent gérer dynamiquement les propriétés du document à l'aide des API Aspose.Diagram. Cette fonctionnalité aide les développeurs à stocker des informations utiles avec le fichier, telles que la date de réception, le traitement, l'horodatage, etc.

{{% alert color="primary" %}}

Aspose.Diagram for .NET écrit directement les informations sur API et le numéro de version dans les documents de sortie.

Veuillez noter que vous ne pouvez pas demander au Aspose.Diagram for .NET de modifier ou de supprimer ces informations des documents de sortie.

{{% /alert %}}

### **Accéder aux propriétés du document**

 Aspose.Diagram Les API prennent en charge les deux types de propriétés de document, intégrées et personnalisées. Aspose.Diagram'[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/Diagram) représente un fichier Visio et, comme un fichier visio, la[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/Diagram) classe peut contenir plusieurs pages, chacune représentée par le[**Page**](https://reference.aspose.com/diagram/net/aspose.diagram/page) classe alors que la collection de pages est représentée par la[**Collection de pages**](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection)classer.

 Utilisez le[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/Diagram)pour accéder aux propriétés du document du fichier comme décrit ci-dessous.

- Pour accéder aux propriétés de document intégrées, utilisez[**diagram.DocumentProps**](https://reference.aspose.com/diagram/net/aspose.diagram/documentproperties).
-  Pour accéder aux propriétés de document personnalisées, utilisez[**diagram.DocumentProps.CustomProps**](https://reference.aspose.com/diagram/net/aspose.diagram/documentproperties/properties/customprops).

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

//// Display Visio version and document modification time at different stages 
Console.WriteLine("Visio Instance Version : " + diagram.Version);
Console.WriteLine("Full Build Number Created : " + diagram.DocumentProps.BuildNumberCreated);
Console.WriteLine("Full Build Number Edited : " + diagram.DocumentProps.BuildNumberEdited);
Console.WriteLine("Date Created : " + diagram.DocumentProps.TimeCreated);
Console.WriteLine("Date Last Edited : " + diagram.DocumentProps.TimeEdited);
Console.WriteLine("Date Last Printed : " + diagram.DocumentProps.TimePrinted);
Console.WriteLine("Date Last Saved : " + diagram.DocumentProps.TimeSaved);
Console.WriteLine("CustomProps Length " + diagram.DocumentProps.CustomProps.Count);

{{< /highlight >}}
```

### **Ajout ou suppression de propriétés de document personnalisées**

Comme nous l'avons décrit précédemment au début de cette rubrique, les développeurs ne peuvent pas ajouter ou supprimer des propriétés intégrées car ces propriétés sont définies par le système, mais il est possible d'ajouter ou de supprimer des propriétés personnalisées car elles sont définies par l'utilisateur.

### **Ajout de propriétés personnalisées**

 Aspose.Diagram Les API ont exposé le[**Ajouter**](https://reference.aspose.com/diagram/net/aspose.diagram/custompropcollection/methods/add) méthode pour la[**CustomPropCollection**](https://reference.aspose.com/diagram/net/aspose.diagram/custompropcollection)class afin d'ajouter des propriétés personnalisées à la collection.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

//// Get CustomProperties of diagram
Aspose.Diagram.CustomPropCollection customProperties = diagram.DocumentProps.CustomProps;
//Set property of CustomProp
Aspose.Diagram.CustomProp customProp = new Aspose.Diagram.CustomProp();
customProp.PropType = Aspose.Diagram.PropType.String;
customProp.CustomValue.ValueString = "Test";
//Add CustomProp to Collection
customProperties.Add(customProp);

{{< /highlight >}}
```

### **Suppression des propriétés personnalisées**

 Pour supprimer les propriétés personnalisées à l'aide de Aspose.Diagram, appelez le[**CustomPropCollection.RemoveCustomPropCollection.Remove**](https://reference.aspose.com/diagram/net/aspose.diagram/custompropcollection/methods/remove)méthode et transmettez le nom de la propriété de document à supprimer.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-RemovingCustomProperties.cs" >}}
