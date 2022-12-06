---
title: Aspose.Diagram for .NET 19.2 Notes de mise à jour
type: docs
weight: 110
url: /fr/net/aspose-diagram-for-net-19-2-release-notes/
---
{{% alert color="primary" %}} 

Cette page contient des notes de version pour[Aspose.Diagram for .NET 19.2](https://www.nuget.org/packages/Aspose.Diagram/19.2.0)

{{% /alert %}} 
## **Améliorations et changements**

|**Clé**|**Sommaire**|**Catégorie**|
|:- |:- |:- |
|DIAGRAMNET-50009|La forme du cœur est mélangée lors de l'exportation du dessin VSD au format de fichier PDF|Renforcement|
|DIAGRAMNET-50010|VSD au format PDF exporte plusieurs lignes en zigzag avec un point simultané au lieu d'une seule ligne de courbe|Renforcement|
|DIAGRAMNET-51257|Ajout de la prise en charge de la ligne NUBRS lors de l'exportation d'un dessin|Renforcement|
|DIAGRAMNET-51611|Impossible d'obtenir Prop.Prompt.Value correctement|Renforcement|
|DIAGRAMNET-50355|Les lignes courbes sont exportées sous forme de lignes droites|Punaise|
|DIAGRAMNET-50702|VSDX vers exportation PDF - les connecteurs incurvés se transforment en droits|Punaise|
|DIAGRAMNET-51348|VSDX en PDF - Rendu incorrect des lettres|Punaise|
|DIAGRAMNET-51399|VSD en PNG - la ligne courbe est convertie en ligne droite|Punaise|
|DIAGRAMNET-51448|VSD en PNG - il manque l'ellipse autour du mot réseau|Punaise|
|DIAGRAMNET-51472|VSD au format PDF - les lignes courbes sont exportées sous forme de lignes droites|Punaise|
|DIAGRAMNET-51507|VSDX vers PNG - les formes ovales remplies manquent dans la sortie|Punaise|
|DIAGRAMNET-51508|VSDX en SVG - les formes ovales remplies manquent dans la sortie|Punaise|
|DIAGRAMNET-51537|VSDX en SVG - les connecteurs incurvés deviennent des connecteurs droits lorsque VSDX est rendu au format PDF|Punaise|
|DIAGRAMNET-51540|Les bords de la forme ont été modifiés en carrés après la conversion|Punaise|
|DIAGRAMNET-51577|VISIO vers SVG - la sortie n'est pas correcte|Punaise|
|DIAGRAMNET-51592|Les lignes courbes se transforment en lignes droites lors de la conversion|Punaise|
|DIAGRAMNET-51600|Les lignes droites deviennent des pointes lors de l'enregistrement d'un diagram sous un autre format|Punaise|
|DIAGRAMNET-51604|VSDX en erreur de conversion PDF - ellipses noires|Punaise|
|DIAGRAMNET-51605|Mettre à jour les références API et ajouter des détails sur la méthode Shape.SetAngle()|Punaise|
|DIAGRAMNET-51610|VSDX en SVG - le texte n'est pas rendu dans la bonne police|Punaise|
## **Public API et modifications incompatibles avec les versions antérieures**
Voici une liste de toutes les modifications apportées au public API, telles que les membres ajoutés, renommés, supprimés ou obsolètes, ainsi que toute modification non rétrocompatible apportée à Aspose.Diagram for .NET. Si vous avez des préoccupations concernant l'un des changements répertoriés, veuillez les signaler dans la[Aspose.Diagram forum d'assistance](https://forum.aspose.com/c/diagram/17).
### **Ajouter InheritProps dans Shape**
Contient les accessoires de la forme dont hérite la forme principale.

{{< highlight "java" >}}

  foreach (Aspose.Diagram.Prop prop in shape.InheritProps)

{

    Console.WriteLine(prop.Name);

    Console.WriteLine(prop.Label.Value);

    Console.WriteLine(prop.Prompt.Value);

    Console.WriteLine(prop.Type.Value.ToString());

    Console.WriteLine(prop.Value.Val);

    Console.WriteLine(prop.Format.Value);

}

{{< /highlight >}}
