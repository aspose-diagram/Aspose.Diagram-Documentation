---
title: Aspose.Diagram for .NET 18.10 Notes de mise à jour
type: docs
weight: 30
url: /fr/net/aspose-diagram-for-net-18-10-release-notes/
---
{{% alert color="primary" %}} 

 Cette page contient des notes de version pour[Aspose.Diagram for .NET 18.10](https://www.nuget.org/packages/Aspose.Diagram/18.10.0).

{{% /alert %}} 
## **Améliorations et changements**

|**Clé**|**Sommaire**|**Catégorie**|
|:- |:- |:- |
|DIAGRAMNET-51527|Les images se perdent après la conversion de VSDM en SVG|Renforcement|
|DIAGRAMNET-51532|VSD au format PDF - L'ombre de l'image n'est pas correcte|Renforcement|
|DIAGRAMNET-51536|L'ombre de la forme a été supprimée après la conversion VSDX en SVG|Renforcement|
|DIAGRAMNET-51544|Le soulignement est supprimé du texte après la conversion de VSDM en SVG|Renforcement|
|DIAGRAMNET-51558|Implémenter Getter pour Shape.ConnectorsType|Renforcement|
|DIAGRAMNET-51520|VDX en HTML - Des lignes supplémentaires apparaissent dans la sortie|Punaise|
|DIAGRAMNET-51521|La police dans le diagram obtient des modifications après avoir enregistré VSD en tant que VSDX|Punaise|
|DIAGRAMNET-51523|VSDX à SVG - Les têtes de flèche manquent|Punaise|
|DIAGRAMNET-51524|VSDM vers SVG - Des croix bleues sont apparues dans le fichier de sortie|Punaise|
|DIAGRAMNET-51525|La forme de la décision passe du losange au carré tandis que VSDM est converti en SVG|Punaise|
|DIAGRAMNET-51528|La forme de la décision passe du losange au carré tandis que VSDM est converti en SVG|Punaise|
|DIAGRAMNET-51529|VSDM en SVG - Lignes pointillées converties en lignes pleines|Punaise|
|DIAGRAMNET-51531|Les formes sont déplacées vers la droite après la conversion de VSDX en SVG|Punaise|
|DIAGRAMNET-51533|Les croix rouges sont apparues après la conversion de VISIO en SVG|Punaise|
|DIAGRAMNET-51534|Un point rouge est apparu dans le coin inférieur gauche de la forme|Punaise|
|DIAGRAMNET-51538|Les images sont perdues après la conversion de VSDX en PDF|Punaise|
|DIAGRAMNET-51541|Le texte est invisible après la conversion de VSDX en SVG|Punaise|
|DIAGRAMNET-51542|Le texte a été supprimé après VSDX en conversion SVG|Punaise|
|DIAGRAMNET-51543|Le format de l'heure et de la date est modifié après VSDM TO SVG|Punaise|
|DIAGRAMNET-51545|VSDX en SVG - Le texte est enveloppé dans la sortie|Punaise|
|DIAGRAMNET-51546|VSDX en SVG - Le texte est enveloppé dans la sortie|Punaise|
|DIAGRAMNET-51547|VSDX en SVG - Le texte est enveloppé dans la sortie|Punaise|
|DIAGRAMNET-51548|VSDX en SVG - Le texte est enveloppé dans la sortie|Punaise|
|DIAGRAMNET-51551|Impossible d'obtenir la couleur de thème correcte des formes|Punaise|
|DIAGRAMNET-51552|Pointes de flèches inversées affichées dans la conversion SVG|Punaise|
|DIAGRAMNET-51559|Problème de redimensionnement du texte lors de la conversion de VSDM en SVG|Punaise|
|DIAGRAMNET-51560|Les lignes de connexion deviennent minces après la conversion en SVG|Punaise|
## **Public API et modifications incompatibles avec les versions antérieures**
Voici une liste de toutes les modifications apportées au public API, telles que les membres ajoutés, renommés, supprimés ou obsolètes, ainsi que toute modification non rétrocompatible apportée à Aspose.Diagram for .NET. Si vous avez des préoccupations concernant l'un des changements répertoriés, veuillez les signaler dans la[Aspose.Diagram forum d'assistance](https://forum.aspose.com/c/diagram/17).
#### **Ajout de InheritLine dans Shape**
Contient les valeurs de mise en forme de ligne pour la forme héritée par le style parent et la forme de base.

{{< highlight "java" >}}

 		Line line = shape.InheritLine;

{{< /highlight >}}


#### **Ajout de GetConnectorsType dans Shape**
Obtenir le type de connecteurs

{{< highlight "java" >}}

 Shapes.GetShape(1).GetConnectorsType()

{{< /highlight >}}

