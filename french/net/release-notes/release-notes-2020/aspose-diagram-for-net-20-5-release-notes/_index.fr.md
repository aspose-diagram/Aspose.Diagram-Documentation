---
title: Aspose.Diagram for .NET 20.5 Notes de mise à jour
type: docs
weight: 30
url: /fr/net/aspose-diagram-for-net-20-5-release-notes/
---
{{% alert color="primary" %}} 

Cette page contient des informations sur les notes de version pour Aspose.Diagram for .NET 20.5.

{{% /alert %}} 
## **Améliorations et changements**
VSD en conversion PDF, le bon alignement du texte des formes n'est pas conservé

|**Clé**|**Sommaire**|**Catégorie**|
|:- |:- |:- |
|DIAGRAMNET-51088|Récupère le nombre de pages incorrect d'un VSD|Renforcement|
|DIAGRAMNET-51731|Déterminez si une forme croise une autre forme dans le diagram|Renforcement|
|DIAGRAMNET-51833|Aspose.Diagram 20.4 : Visio La version du document n'est pas prise en charge|Renforcement|
|DIAGRAMNET-50361|VSD en conversion PDF, le bon alignement du texte des formes n'est pas conservé|Punaise|
|DIAGRAMNET-50955|Les éléments de texte des formes de diamant sont déplacés lors de la conversion d'un VSDX en PNG|Punaise|
|DIAGRAMNET-50990|De plus, les signes négatif et dollar ne sont pas correctement alignés lors de la conversion d'un VSDX en PNG|Punaise|
|DIAGRAMNET-51815|Une grande quantité de lignes de texte en forme pourrait créer un déplacement évident dans la partie inférieure|Punaise|
|DIAGRAMNET-51820|Le filigrane d'évaluation ne tient pas dans une page|Punaise|
|DIAGRAMNET-51821|Visio vers Html - problèmes d'image et de liens dans la sortie|Punaise|
|DIAGRAMNET-51823|Lors de la conversion de Visio en SVG. Certaines images ont un problème Icône manquante|Punaise|
|DIAGRAMNET-51824|Lors de la conversion de Visio en SVG. Mauvais alignement du contenu|Punaise|
|DIAGRAMNET-51826|Lors de la conversion de Visio en SVG. Icône manquante|Punaise|
|DIAGRAMNET-51827|Lors de la conversion de Visio en SVG - Code QR manquant|Punaise|
|DIAGRAMNET-51828|Lors de la conversion de Visio en SVG - icône PDF manquante|Punaise|
|DIAGRAMNET-51829|Lors de la conversion de Visio en SVG - Icône perdue (manquante)|Punaise|
|DIAGRAMNET-51830|Lors de la conversion de Visio en SVG - Image perdue (manquante)|Punaise|
|DIAGRAMNET-51831|Visio vers HTML - problèmes d'image et de liens dans la sortie|Punaise|
|DIAGRAMNET-51834|Visio enregistrer HTML - mauvais connecteurs|Punaise|

## **Public API et modifications incompatibles avec les versions antérieures**
Vous trouverez ci-dessous une liste de toutes les modifications apportées au public API, telles que les membres ajoutés, renommés, supprimés ou obsolètes, ainsi que toute modification non rétrocompatible apportée à Aspose.Diagram for .NET. Si vous avez des inquiétudes concernant l'un des changements répertoriés, veuillez le signaler sur le forum d'assistance Aspose.Diagram.
### **Ajoute IsIntersect dans Shape**
- Indique si cette forme croise une autre forme.

{{< highlight "java" >}}

Shape s1 = diagram.Pages[0].Shapes.GetShape(1);

Shape s2 = diagram.Pages[0].Shapes.GetShape(2);

bool isIntersect = s1.IsIntersect(s2);

{{< /highlight >}}



