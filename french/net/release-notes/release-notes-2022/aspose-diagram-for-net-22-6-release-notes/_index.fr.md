---
title: Aspose.Diagram for .NET 22.6 Notes de mise à jour
type: docs
weight: 22
url: /fr/net/aspose-diagram-for-net-22-6-release-notes/
---
{{% alert color="primary" %}} 

Cette page contient des informations sur les notes de version pour Aspose.Diagram for .NET 22.6.

{{% /alert %}} 
## **Améliorations et changements**

|**Clé**|**Sommaire**|**Catégorie**|
|:- |:- |:- |
|DIAGRAMNET-52826|Lien brisé lors de l'enregistrement du VSDM au format PDF|Renforcement|
|DIAGRAMNET-52851|Certaines formes perdent leur courbe après conversion en svg|Renforcement|
|DIAGRAMNET-52858|Qualité d'image en HTML|Renforcement|
|DIAGRAMNET-52825|Problème d'exportation vers HTML|Punaise|
|DIAGRAMNET-52832|Visio en PDF/SVG - La position du texte pivoté a été modifiée|Punaise|
|DIAGRAMNET-52840|Éléments flous dans l'aperçu HTML|Punaise|
|DIAGRAMNET-52842|La page d'ajustement automatique ne s'adapte pas automatiquement|Punaise|
|DIAGRAMNET-52849|Images raster non réduites après la conversion|Punaise|
|DIAGRAMNET-52852|VSD Erreur d'ouverture - Aspose.Diagram.DiagramException|Punaise|

## **Public API et modifications incompatibles avec les versions antérieures**
Vous trouverez ci-dessous une liste de toutes les modifications apportées au public API, telles que les membres ajoutés, renommés, supprimés ou obsolètes, ainsi que toute modification non rétrocompatible apportée à Aspose.Diagram for .NET. Si vous avez des inquiétudes concernant l'un des changements répertoriés, veuillez le signaler sur le forum d'assistance Aspose.Diagram.
### **Ajoute une résolution dans HTMLSaveOptions**
- Obtient ou définit la résolution du code HTML généré, en points par pouce.

{{< highlight "java" >}}
HTMLSaveOptions option = new HTMLSaveOptions();
option.Resolution = 96;
{{< /highlight >}}
