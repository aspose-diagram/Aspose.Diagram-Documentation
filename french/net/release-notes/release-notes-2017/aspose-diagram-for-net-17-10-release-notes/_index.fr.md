---
title: Aspose.Diagram for .NET 17.10 Notes de mise à jour
type: docs
weight: 30
url: /fr/net/aspose-diagram-for-net-17-10-release-notes/
---
{{% alert color="primary" %}} 

 Cette page contient des notes de version pour[Aspose.Diagram for .NET 17.10](https://www.nuget.org/packages/Aspose.Diagram/17.10.0).

{{% /alert %}} 
## **Améliorations et changements**

|**Clé**|**Sommaire**|**Catégorie**|
|:- |:- |:- |
|DIAGRAMNET-51349|Ajout de la prise en charge de la conversion d'un dessin en image de la même zone qu'un PDF|Renforcement|
|DIAGRAMNET-51352|Accéder aux fichiers intégrés|Renforcement|
|DIAGRAMNET-51085|Les formules sont perdues sous l'onglet contrôles de Shapesheet lors de l'enregistrement dans VSDX|Punaise|
|DIAGRAMNET-51094|Conserver les paramètres par défaut sous l'onglet de contrôle lors du placement d'une forme trapézoïdale|Punaise|
|DIAGRAMNET-51355|VSDX en PDF - les éléments de texte sont mal placés|Punaise|
|DIAGRAMNET-51356|VSDX en HTML - les éléments de texte sont mal placés|Punaise|
|DIAGRAMNET-51357|Ouvrir et enregistrer la routine de VSDX - date manquante et modifier les attributs de date des annotations|Punaise|
|` `DIAGRAMNET-51358|Une erreur de pointeur nul s'est produite lors du chargement du dessin VSDX|Punaise|
|DIAGRAMNET-51359|Erreur dans la liste des auteurs d'éléments après le chargement d'un VSDX|Punaise|
|DIAGRAMNET-51361|VSDX à VDX - la police de texte incorrecte de la forme|Punaise|
|DIAGRAMNET-51363|Ouvrir et enregistrer la routine de VSDX - La section des onglets se transforme en une balise auto-fermée|Punaise|
|DIAGRAMNET-51365|VSD vers PNG - disposition incorrecte des formes|Punaise|
|DIAGRAMNET-51367|VSD importation de dessin - une erreur dans l'élément maître|Punaise|
|DIAGRAMNET-51368|VSD vers PNG - une erreur de débordement s'est produite|Punaise|
|DIAGRAMNET-51369|VSD au format PDF - éléments de texte mal placés en bas|Punaise|
|DIAGRAMNET-51371|VSDX à VSDX - des éléments de texte supplémentaires sont ajoutés|Punaise|
|DIAGRAMNET-51373|La routine d'ouverture et de sauvegarde d'un dessin VSDX manque une police de texte asiatique|Punaise|
## **Public API et modifications incompatibles avec les versions antérieures**
Voici une liste de toutes les modifications apportées au public API, telles que les membres ajoutés, renommés, supprimés ou obsolètes, ainsi que toute modification non rétrocompatible apportée à Aspose.Diagram for .NET. Si vous avez des préoccupations concernant l'un des changements répertoriés, veuillez les signaler dans la[Aspose.Diagram forum d'assistance](https://forum.aspose.com/c/diagram/17).
### **Ajoute SameAsPdfConversionArea dans ImageSaveOptions**
Il spécifie s'il faut enregistrer la zone de la même manière que PDF.

{{< highlight "java" >}}

 string dataDir = @"C:\temp\";

// load a drawing

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// specify image save options

Aspose.Diagram.Saving.ImageSaveOptions opts = new Aspose.Diagram.Saving.ImageSaveOptions(SaveFileFormat.PNG);

opts.SameAsPdfConversionArea = true;

{{< /highlight >}}
