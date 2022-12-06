---
title: Aspose.Diagram for .NET 20.1 Notes de mise à jour
type: docs
weight: 70
url: /fr/net/aspose-diagram-for-net-20-1-release-notes/
---
{{% alert color="primary" %}} 

Cette page contient des informations sur les notes de version pour Aspose.Diagram for .NET 20.1.

{{% /alert %}} 
## **Améliorations et changements**

|**Clé**|**Sommaire**|**Catégorie**|
|:- |:- |:- |
|DIAGRAMNET-51198|L'ombre sur le bouton de lien hypertexte n'est pas rendue correctement lors de l'enregistrement de VSDM en SVG|Renforcement|
|DIAGRAMNET-51526|VSDX en PDF - Remplissage dégradé pour les pointes de flèches perdues dans le PDF résultant|Renforcement|
|DIAGRAMNET-51539|Le dégradé dans les formes a perdu en sortie SVG|Renforcement|
|DIAGRAMNET-50705|VSD vers exportation SVG - Les formes de type méta se transforment en symboles désordonnés|Punaise|
|DIAGRAMNET-51664|Le fichier est corrompu après la suppression du thème inutilisé|Punaise|
|DIAGRAMNET-51665|Les images sont affichées sous forme de X après la suppression des thèmes inutilisés|Punaise|
|DIAGRAMNET-51684|Lors de la suppression des formes et des styles principaux inutilisés, seule l'image a un problème|Punaise|
|DIAGRAMNET-51726|Image d'arrière-plan manquante (PowerPoint est ajouté dans le VISIO) lors de la suppression des formes et des styles principaux inutilisés|Punaise|
|DIAGRAMNET-51737|Visio vers Html - Problème de taille d'image|Punaise|
|DIAGRAMNET-51743|Suppression des informations privées de Visio - problème de taille de document Visio|Punaise|
|DIAGRAMNET-51745|Une erreur étrange se produit dans l'application WPF lors de la conversion de VSD en VSDX|Punaise|

## **Public API et modifications incompatibles avec les versions antérieures**
- Pages ajoutées à LoadOptions - Spécifie l'index des pages à charger.



{{< highlight "java" >}}

Aspose.Diagram.LoadOptions options = new Aspose.Diagram.LoadOptions(LoadFileFormat.VSDX);

options.Pages = new ArrayList();

options.Pages.Add(0);

{{< /highlight >}}

- Ajout de SetFontSources dans FontConfigs - Définit les sources de polices

{{< highlight "java" >}}

Aspose.Diagram.MemoryFontSource sc1 = new Aspose.Diagram.MemoryFontSource(b);

Aspose.Diagram.MemoryFontSource sc2 = new Aspose.Diagram.MemoryFontSource(b);

Aspose.Diagram.MemoryFontSource[]sc = new Aspose.Diagram.MemoryFontSource[]{ sc1, sc2 };

Aspose.Diagram.FontConfigs.SetFontSources(sc); 

{{< /highlight >}}
