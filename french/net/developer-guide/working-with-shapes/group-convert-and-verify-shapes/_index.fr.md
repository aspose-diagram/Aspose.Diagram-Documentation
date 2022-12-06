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

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-GroupShapes-GroupShapes.cs" >}}
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
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-SaveVisioShapeInOtherFormats-SaveVisioShapeInOtherFormats.cs" >}}
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

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-VerifyConnectedOrGluedShapes-VerifyConnectedOrGluedShapes.cs" >}}
## **Vérifiez si la forme Visio se trouve dans un groupe de formes**
Aspose.Diagram for .NET API permet aux développeurs de vérifier que la forme Visio est dans un groupe de formes ou non.
### **Vérification de la forme dans le groupe de formes**
La[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)La classe offre des propriétés IsInGroup pour déterminer si la forme Visio est dans une forme de groupe.
#### **Vérification de la forme dans l'exemple de programmation du groupe de formes**
Le morceau de code suivant vérifie si la forme est dans une forme de groupe.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-VerifyShapeIsInGroup-VerifyShapeIsInGroup.cs" >}}
