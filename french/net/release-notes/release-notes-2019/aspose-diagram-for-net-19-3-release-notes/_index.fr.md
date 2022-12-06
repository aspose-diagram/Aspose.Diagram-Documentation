---
title: Aspose.Diagram for .NET 19.3 Notes de mise à jour
type: docs
weight: 100
url: /fr/net/aspose-diagram-for-net-19-3-release-notes/
---
{{% alert color="primary" %}} 

Cette page contient des notes de version pour[Aspose.Diagram for .NET 19.3](https://www.nuget.org/packages/Aspose.Diagram/19.3.0)

{{% /alert %}} 
## **Améliorations et changements**

|**Clé**|**Sommaire**|**Catégorie**|
|:- |:- |:- |
|DIAGRAMNET-50930|Ajout de la prise en charge de la récupération des répertoires de polices communs sur les systèmes d'exploitation|Renforcement|
|DIAGRAMNET-51614|Obtenir toutes les valeurs d'accessoires pour une forme|Renforcement|
|DIAGRAMNET-50214|Conversion VSD en PDF - Les lignes courbes deviennent une ligne droite|Punaise|
|DIAGRAMNET-50240|Conversion VSD en PDF - Mauvaise disposition des connecteurs dynamiques|Punaise|
|DIAGRAMNET-50703|VSDX vers exportation PDF - Il manque un connecteur dynamique|Punaise|
|DIAGRAMNET-50704|VSD vers exportation PDF - Les formes de type méta se transforment en symboles désordonnés|Punaise|
|DIAGRAMNET-51535|VSDM en SVG - La police passe de Sans à Serif en SVG|Punaise|
|DIAGRAMNET-51574|VSDX à PNG - Certaines formes sont rendues incorrectes dans la sortie PNG|Punaise|
|DIAGRAMNET-51608|L'habillage du texte ne fonctionne pas comme prévu|Punaise|
|DIAGRAMNET-51609|Les formes sont décalées vers la gauche lorsque Diagram est copié dans PowerPoint Slide|Punaise|
|DIAGRAMNET-51617|Visio au format PDF - Les valeurs basées sur les données externes ne s'affichent pas correctement|Punaise|
|DIAGRAMNET-51619|Visio en PDF - Date/Heure/Distance incorrectes en PDF|Punaise|
|DIAGRAMNET-51621|Visio en PDF - L'image d'arrière-plan est déformée et la page supplémentaire est présente en PDF|Punaise|
## **Public API et modifications incompatibles avec les versions antérieures**
Voici une liste de toutes les modifications apportées au public API, telles que les membres ajoutés, renommés, supprimés ou obsolètes, ainsi que toute modification non rétrocompatible apportée à Aspose.Diagram for .NET. Si vous avez des préoccupations concernant l'un des changements répertoriés, veuillez les signaler dans la[Aspose.Diagram forum d'assistance](https://forum.aspose.com/c/diagram/17).
### **Ajoute GetDefaultFontDir dans Diagram**
Obtenir le chemin du dossier des polices par défaut

{{< highlight "java" >}}

  string str =  diagram.GetDefaultFontDir();

{{< /highlight >}}
