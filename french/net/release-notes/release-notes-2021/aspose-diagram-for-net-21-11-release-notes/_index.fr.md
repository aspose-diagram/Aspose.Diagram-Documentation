---
title: Aspose.Diagram for .NET 21.11 Notes de mise à jour
type: docs
weight: 2
url: /fr/net/aspose-diagram-for-net-21-11-release-notes/
---
{{% alert color="primary" %}} 

Cette page contient des informations sur les notes de version pour Aspose.Diagram for .NET 21.11.

{{% /alert %}} 
## **Améliorations et changements**

|**Clé**|**Sommaire**|**Catégorie**|
|:- |:- |:- |
|DIAGRAMNET-51111|Le remplissage dégradé des cercles est incorrect lors de la conversion d'un VDX en EMF|Renforcement|
|DIAGRAMNET-52377|Ajout de la prise en charge du chargement vsd avec l'ancienne version 3|Renforcement|
|DIAGRAMNET-51364|VSDX en PNG - il manque le texte de l'objet OLE Embedded|Punaise|
|DIAGRAMNET-52329|VSDX en HTML - Les emojis ne sont pas présents dans la sortie|Punaise|
|DIAGRAMNET-52345|Les en-têtes de pied de page sont perdus après l'enregistrement du fichier Diagram|Punaise|
|DIAGRAMNET-52349|Visio en HTML - Les bords gauche et droit sont coupés|Punaise|
|DIAGRAMNET-52374|ArgumentOutOfRangeException lors de l'enregistrement au format PDF|Punaise|
|DIAGRAMNET-52386|Pourquoi certaines pages diagram peuvent être dupliquées et d'autres ne peuvent pas utiliser Page.Copy() ?|Punaise|

## **Public API et modifications incompatibles avec les versions antérieures**
Vous trouverez ci-dessous une liste de toutes les modifications apportées au public API, telles que les membres ajoutés, renommés, supprimés ou obsolètes, ainsi que toute modification non rétrocompatible apportée à Aspose.Diagram for .NET. Si vous avez des inquiétudes concernant l'un des changements répertoriés, veuillez le signaler sur le forum d'assistance Aspose.Diagram.


### **Ajoute PresetTheme dans Shape**
- Appliquez un thème prédéfini à cette forme.

{{< highlight "java" >}}

shape.PresetTheme = PresetThemeValue.Bubble;

{{< /highlight >}}


### **Ajoute PresetThemeVariant dans Shape**
- Appliquer une variante de thème prédéfinie à cette forme

{{< highlight "java" >}}

shape.PresetThemeVariant = PresetThemeVariantValue.Variant1;

{{< /highlight >}}

### **Ajoute PresetThemeQuickStyle dans Shape**
- Appliquer un style rapide de variante de thème prédéfini à cette forme

{{< highlight "java" >}}

 shape.PresetThemeQuickStyle = PresetQuickStyleValue.VariantStyle1;

{{< /highlight >}}
