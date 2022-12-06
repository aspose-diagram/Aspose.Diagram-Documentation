---
title: Aspose.Diagram for .NET 18.9 Notes de mise à jour
type: docs
weight: 40
url: /fr/net/aspose-diagram-for-net-18-9-release-notes/
---
{{% alert color="primary" %}} 

 Cette page contient des notes de version pour[Aspose.Diagram for .NET 18.9](https://www.nuget.org/packages/Aspose.Diagram/18.9.0).

{{% /alert %}} 
## **Améliorations et changements**

|**Clé**|**Sommaire**|**Catégorie**|
|:- |:- |:- |
|DIAGRAMNET-51509|VSDX à PNG - Opacité des lignes perdue dans l'image de sortie|Renforcement|
|DIAGRAMNET-51510|VSDX à SVG - Opacité de la ligne perdue dans l'image de sortie|Renforcement|
|DIAGRAMNET-51516|Fusionner plusieurs fichiers VISIO en une seule sortie|Renforcement|
|DIAGRAMNET-50272|VSD en conversion SVG - Certains points de connexion ont une position et une taille incorrectes|Punaise|
|DIAGRAMNET-50273|VSD vers SVG - L'alignement des éléments de texte de forme est incorrect|Punaise|
|DIAGRAMNET-50487|VSD en HTML - Le caractère barre oblique entre la valeur est mal placé|Punaise|
|DIAGRAMNET-50975|VSDX au format PDF - La couleur de fond de la forme est noire|Punaise|
|DIAGRAMNET-50976|VSDX vers HTML - La couleur de fond de la forme est noire|Punaise|
|DIAGRAMNET-50980|VSDX vers PNG - Les chiffres à l'intérieur des losanges sont mal placés|Punaise|
|DIAGRAMNET-51129|Les éléments de texte ne sont pas correctement alignés lors de la conversion d'un VSD en PDF|Punaise|
|DIAGRAMNET-51511|Pointes de flèches supplémentaires dans la conversion PNG|Punaise|
|DIAGRAMNET-51512|Pointes de flèches supplémentaires affichées dans la conversion SVG|Punaise|
## **Public API et modifications incompatibles avec les versions antérieures**
Voici une liste de toutes les modifications apportées au public API, telles que les membres ajoutés, renommés, supprimés ou obsolètes, ainsi que toute modification non rétrocompatible apportée à Aspose.Diagram for .NET. Si vous avez des préoccupations concernant l'un des changements répertoriés, veuillez les signaler dans la[Aspose.Diagram forum d'assistance](https://forum.aspose.com/c/diagram/17).
#### **Ajout de la méthode Combine dans la classe Diagram**
Combine un objet Diagram avec un autre objet Diagram.

{{< highlight "java" >}}

             Diagram diagramF = new Diagram( "f.vsdx");

            Diagram diagramS = new Diagram( "s.vsdx");

            diagramF.Combine(diagramS);

{{< /highlight >}}
