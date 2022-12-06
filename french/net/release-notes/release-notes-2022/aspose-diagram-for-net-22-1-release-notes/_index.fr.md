---
title: Aspose.Diagram for .NET 22.1 Notes de mise à jour
type: docs
weight: 27
url: /fr/net/aspose-diagram-for-net-22-1-release-notes/
---
{{% alert color="primary" %}} 

Cette page contient des informations sur les notes de version pour Aspose.Diagram for .NET 22.1.

{{% /alert %}} 
## **Améliorations et changements**

|**Clé**|**Sommaire**|**Catégorie**|
|:- |:- |:- |
|DIAGRAMNET-50560|Prise en charge de l'enregistrement de diagrammes au format HTML avec ou sans ressources intégrées|Renforcement|
|DIAGRAMNET-52499|Ajout de la prise en charge de l'enregistrement du code HTML dans un flux unique|Renforcement|
|DIAGRAMNET-50562|VSDX au format PDF - Les formes manquent dans la sortie|Punaise|
|DIAGRAMNET-50780|Les bordures des tableaux ne sont pas visibles lors de l'enregistrement d'un VSDX au format PDF|Punaise|
|DIAGRAMNET-50962|Les lignes de bordure des tableaux sont manquantes lors de la conversion d'un VSDX en PNG|Punaise|
|DIAGRAMNET-50992|La bordure gauche du tableau n'est pas visible lors de la conversion d'un VSDX en PDF|Punaise|
|DIAGRAMNET-51034|L'ombrage des formes est manquant lors de la conversion d'un VSDX en PDF|Punaise|
|DIAGRAMNET-51186|Disposition incorrecte des formes de type méta lors de la conversion d'un VSD en PDF|Punaise|
|DIAGRAMNET-51226|Aspose.Diagram 17.3.0 : L'enregistrement dans le flux HTML n'intègre pas de ressources externes|Punaise|
|DIAGRAMNET-52506|Page.Copy() ne copie pas les modifications du développeur|Punaise|

## **Public API et modifications incompatibles avec les versions antérieures**
Vous trouverez ci-dessous une liste de toutes les modifications apportées au public API, telles que les membres ajoutés, renommés, supprimés ou obsolètes, ainsi que toute modification non rétrocompatible apportée à Aspose.Diagram for .NET. Si vous avez des inquiétudes concernant l'un des changements répertoriés, veuillez le signaler sur le forum d'assistance Aspose.Diagram.


### **Ajoute SaveAsSingleFile dans HTMLSaveOptions**
- Indique si enregistrer le HTML en tant que fichier unique.

{{< highlight "java" >}}

    HTMLSaveOptions ho = new HTMLSaveOptions();
    ho.SaveAsSingleFile = true;

{{< /highlight >}}