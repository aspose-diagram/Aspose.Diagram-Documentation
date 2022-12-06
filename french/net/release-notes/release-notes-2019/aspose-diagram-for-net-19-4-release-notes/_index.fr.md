---
title: Aspose.Diagram for .NET 19.4 Notes de mise à jour
type: docs
weight: 90
url: /fr/net/aspose-diagram-for-net-19-4-release-notes/
---
{{% alert color="primary" %}} 

Cette page contient des notes de version pour[Aspose.Diagram for .NET 19.4](https://www.nuget.org/packages/Aspose.Diagram/19.4.0)

{{% /alert %}} 
## **Améliorations et changements**

|**Clé**|**Sommaire**|**Catégorie**|
|:- |:- |:- |
|DIAGRAMNET-51602|L'objet XSLX intégré est corrompu après manipulation|Renforcement|
|DIAGRAMNET-51625|Les données Excel externes dans les fichiers .vsdx sont supprimées lors de la ré-enregistrement Diagram|Renforcement|
|DIAGRAMNET-51626|API ne traite pas les données Excel|Renforcement|
|DIAGRAMNET-51627|Extraire les données de forme sur la base de la formule Dependson|Renforcement|
|DIAGRAMNET-51629|Agrandir une page pour l'adapter à un dessin ne semble pas fonctionner|Renforcement|
|DIAGRAMNET-51176|La barre de titre du dégradé est modifiée lors de la conversion d'un VSDM en SVG|Punaise|
|DIAGRAMNET-51404|VSD à Image - La couleur de la forme est sombre|Punaise|
|DIAGRAMNET-51473|VDX au format PDF - La couleur d'arrière-plan incorrecte|Punaise|
|DIAGRAMNET-51475|VSDX au format PDF - Les dégradés sont rendus à l'envers|Punaise|
|DIAGRAMNET-51616|Visio en PDF - Le dégradé est rendu à l'envers dans le PDF de sortie|Punaise|
|DIAGRAMNET-51630|VSDX en HTML - La couleur d'arrière-plan des formes n'est pas présente dans la sortie|Punaise|
|DIAGRAMNET-51631|VSDX au format PDF - La couleur d'arrière-plan des formes n'est pas présente dans la sortie|Punaise|
|DIAGRAMNET-51632|VSD en SVG - Impossible de convertir l'objet de type ' ' en type ' ' Une exception s'est produite|Punaise|

## **Public API et modifications incompatibles avec les versions antérieures**
Voici une liste de toutes les modifications apportées au public API, telles que les membres ajoutés, renommés, supprimés ou obsolètes, ainsi que toute modification non rétrocompatible apportée à Aspose.Diagram for .NET. Si vous avez des préoccupations concernant l'un des changements répertoriés, veuillez les signaler dans la[Aspose.Diagram forum d'assistance](https://forum.aspose.com/c/diagram/17).
### **Ajoute l'énumération RemoveHiddenInfoItem**
Spécifie la suppression des informations masquées pour le diagram.
### **Ajoute RemoveHiddenInfoItem dans Diagram**
Supprimez les informations non utilisées.

{{< highlight "java" >}}

diagram.RemoveHiddenInformation((int)(RemoveHiddenInfoItem.Shapes | RemoveHiddenInfoItem.Masters));

{{< /highlight >}}
