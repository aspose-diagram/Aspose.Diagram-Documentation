---
title: Aspose.Diagram for .NET 19.5 Notes de mise à jour
type: docs
weight: 80
url: /fr/net/aspose-diagram-for-net-19-5-release-notes/
---
{{% alert color="primary" %}} 

Cette page contient des notes de version pour[Aspose.Diagram for .NET 19.5](https://www.nuget.org/packages/Aspose.Diagram/19.5.0)

{{% /alert %}} 
## **Améliorations et changements**

|**Clé**|**Sommaire**|**Catégorie**|
|:- |:- |:- |
|DIAGRAMNET-51606|Détectez et supprimez les thèmes, les graphiques de données et les styles inutilisés des diagrammes Visio|Renforcement|
|DIAGRAMNET-51637|La forme imbriquée à l'intérieur d'un conteneur groupé n'est pas conservée correctement|Renforcement|
|DIAGRAMNET-51638|Impossible d'obtenir Prop.Value.Val lorsque la valeur est un entier|Renforcement|
|DIAGRAMNET-51640|Déterminer les styles inutilisés dans un fichier Visio|Renforcement|
|DIAGRAMNET-50051|Conversion VSDX en PDF, flèche de connexion manquante avec texte mal placé|Punaise|
|DIAGRAMNET-50052|Conversion VSDX en PDF, formes avec une couleur de texte de police incorrecte|Punaise|
|DIAGRAMNET-51179|Ombrage incorrect sur un bouton e-mail lors de la conversion d'un VSDM en SVG|Punaise|
|DIAGRAMNET-51190|Affichage incorrect de la forme hyperliée lors de l'enregistrement d'un VDX en SVG|Punaise|
|DIAGRAMNET-51194|Rendu incorrect d'une icône lors de l'enregistrement d'un VDX en SVG|Punaise|
|DIAGRAMNET-51254|Ombrage incorrect dans la barre supérieure lors de la conversion d'un VSDM en SVG|Punaise|
|DIAGRAMNET-51618|Visio en PDF - Format de date erroné et données manquantes|Punaise|
|DIAGRAMNET-51628|Valeur de texte incorrecte pour le texte par défaut supprimé dans les diagrammes .vsdx|Punaise|
|DIAGRAMNET-51634|Visio vers SVG - Mauvais z-index de certaines formes en sortie|Punaise|
|DIAGRAMNET-51636|Visio vers SVG - tous les éléments de chemin ne sont pas correctement exportés en tant qu'éléments rect|Punaise|
|DIAGRAMNET-51641|Une image supplémentaire s'affiche lors de la ré-enregistrement Visio avec API|Punaise|
## **Public API et modifications incompatibles avec les versions antérieures**
Voici une liste de toutes les modifications apportées au public API, telles que les membres ajoutés, renommés, supprimés ou obsolètes, ainsi que toute modification non rétrocompatible apportée à Aspose.Diagram for .NET. Si vous avez des préoccupations concernant l'un des changements répertoriés, veuillez les signaler dans la[Aspose.Diagram forum d'assistance](https://forum.aspose.com/c/diagram/17).
### **Ajoute GetUnusedStyles dans Diagram**
Obtenez des styles inutilisés.

{{< highlight "java" >}}

  StyleSheetCollection unused = diagram.GetUnusedStyles();

{{< /highlight >}}
