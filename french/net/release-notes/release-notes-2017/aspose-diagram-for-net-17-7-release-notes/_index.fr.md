---
title: Aspose.Diagram for .NET 17.7 Notes de mise à jour
type: docs
weight: 60
url: /fr/net/aspose-diagram-for-net-17-7-release-notes/
---
{{% alert color="primary" %}} 

 Cette page contient des notes de version pour[Aspose.Diagram for .NET 17.7](https://www.nuget.org/packages/Aspose.Diagram/17.7.0).

{{% /alert %}} 
## **Améliorations et changements**

|**Clé**|**Sommaire**|**Catégorie**|
|:- |:- |:- |
|DIAGRAMNET-51204|Le format du papier de l'imprimante est modifié après l'enregistrement diagram.|Renforcement|
|DIAGRAMNET-51230|Valeurs incorrectes des marges de page.|Renforcement|
|DIAGRAMNET-51274|Ajout de la prise en charge de l'insertion de commentaires au niveau de la forme.|Renforcement|
|DIAGRAMNET-51297|Entrée VDX - lecture incorrecte de SolutionXML.|Renforcement|
|DIAGRAMNET-51061|Formes manquantes lors de la conversion d'un VST en PNG.|Punaise|
|DIAGRAMNET-51262|Éléments de texte déplacés lors de la conversion d'un VSDM en SVG.|Punaise|
|DIAGRAMNET-51276|VSD à SVG - toutes les icônes ne sont pas visibles correctement.|Punaise|
|DIAGRAMNET-51277|VSDM à SVG - Ombre de formes manquante.|Punaise|
|DIAGRAMNET-51279|Un caractère manquant lors de la conversion d'un VSD en PDF.|Punaise|
|DIAGRAMNET-51282|Certains fichiers vdx sont corrompus après l'enregistrement.|Punaise|
|DIAGRAMNET-51284-|DiagramException se produit lors du chargement du fichier vsdx.|Punaise|
|DIAGRAMNET-51285|VSD à PNG - tous les éléments de texte sont manquants.|Punaise|
|DIAGRAMNET-51286|VSD à PNG - le rendu partiel d'une forme.|Punaise|
|DIAGRAMNET-51288|Erreur de valeur de couleur non valide lors de la conversion d'un VSDX en PNG.|Punaise|
|DIAGRAMNET-51289|L'icône des commentaires au niveau de la page n'affiche pas de texte.|Punaise|
|DIAGRAMNET-51290|Aspose.Diagram bogue dans la méthode SetWidth.|Punaise|
|DIAGRAMNET-51291|Sortie VSDX - mise en page incorrecte lors de la mise en ligne droite des lignes de connexion.|Punaise|
|DIAGRAMNET-51292|Sortie VSDX - l'élément de texte des lignes de connexion est mal placé.|Punaise|
|DIAGRAMNET-51293|VSDX à SVG - une marque supplémentaire apparaît avec les formes.|Punaise|
|DIAGRAMNET-51294|VSDM à SVG - une marque supplémentaire apparaît avec les formes.|Punaise|
## **Public API et modifications incompatibles avec les versions antérieures**
Voici une liste de toutes les modifications apportées au public API, telles que les membres ajoutés, renommés, supprimés ou obsolètes, ainsi que toute modification non rétrocompatible apportée à Aspose.Diagram for .NET. Si vous avez des préoccupations concernant l'un des changements répertoriés, veuillez les signaler dans la[Aspose.Diagram forum d'assistance](https://forum.aspose.com/c/diagram/17).
### **La méthode AddComment est ajoutée dans la classe Page**
Une méthode AddComment surchargée, exposée par la classe Page prend une instance de classe Shape et la chaîne de texte du commentaire.

{{< highlight "java" >}}

 // load diagram

Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

// retrieve page by name

Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// retrieve shape by ID

Aspose.Diagram.Shape shape = page.Shapes.GetShape(12);

page.AddComment(shape, "Hello");

// save diagram

diagram.Save(@"c:\temp\Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **Exemples d'utilisation**
Veuillez consulter la liste des rubriques d'aide ajoutées dans les documents Wiki Aspose.Diagram :

1. [Ajouter un commentaire au niveau de la forme dans le dessin Visio](/diagram/fr/net/working-with-comments/#workingwithcomments-addashape-levelcommentinvisiodrawing)
