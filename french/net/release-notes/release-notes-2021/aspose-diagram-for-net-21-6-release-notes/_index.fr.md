---
title: Aspose.Diagram for .NET 21.6 Notes de mise à jour
type: docs
weight: 7
url: /fr/net/aspose-diagram-for-net-21-6-release-notes/
---
{{% alert color="primary" %}} 

Cette page contient des informations sur les notes de version pour Aspose.Diagram for .NET 21.6.

{{% /alert %}} 
## **Améliorations et changements**

|**Clé**|**Sommaire**|**Catégorie**|
|:- |:- |:- |
|DIAGRAMNET-52007|Performance lors de l'initialisation d'un objet diagram|Renforcement|
|DIAGRAMNET-52008|Performance lors de l'initialisation d'un objet diagram|Renforcement|
|DIAGRAMNET-52027|La qualité des formes n'est pas bonne dans le fichier SVG exporté|Renforcement|
|DIAGRAMNET-52033|Enregistrement de formes au problème HTML|Punaise|
|DIAGRAMNET-52035|"Eof sans exception." exception lors de l'ouverture du fichier VSDX|Punaise|
|DIAGRAMNET-52041|Échec de l'enregistrement de certaines formes à partir du fichier VSS|Punaise|
|DIAGRAMNET-52042|"Le paramètre n'est pas valide." exception lors du rendu du fichier VSD en HTML|Punaise|
|DIAGRAMNET-52043|"La référence d'objet n'est pas définie à une instance d'un objet." exception lors de l'enregistrement de la forme à partir du fichier VSSX|Punaise|

## **Public API et modifications incompatibles avec les versions antérieures**
Vous trouverez ci-dessous une liste de toutes les modifications apportées au public API, telles que les membres ajoutés, renommés, supprimés ou obsolètes, ainsi que toute modification non rétrocompatible apportée à Aspose.Diagram for .NET. Si vous avez des inquiétudes concernant l'un des changements répertoriés, veuillez le signaler sur le forum d'assistance Aspose.Diagram.
### **Ajout de EmfRenderSetting dans SVGSaveOptions**
- Paramètre pour le rendu du métafichier Emf

{{< highlight "java" >}}

SVGSaveOptions o = new SVGSaveOptions();
o.EmfRenderSetting = Aspose.Diagram.EmfRenderSetting.EmfPlusPrefer;

{{< /highlight >}}
### **Ajoute InheritTextBlock dans Shape**
- Contient les valeurs de bloc de texte pour la forme héritée par le style parent et la forme principale.



{{< highlight "java" >}}

shape.InheritTextBlock

{{< /highlight >}}





