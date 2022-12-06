---
title: Aspose.Diagram for .NET 20.8 Notes de mise à jour
type: docs
weight: 14
url: /fr/net/aspose-diagram-for-net-20-8-release-notes/
---
{{% alert color="primary" %}}

Cette page contient des informations sur les notes de version pour Aspose.Diagram for .NET 20.8.

{{% /alert %}}
## **Améliorations et changements**  ##

|**Clé**|**Sommaire**|**Catégorie**|
|:- |:- |:- |
|DIAGRAMNET-51886|Créez la possibilité d'insérer des objets Ole tels que des mots, des cellules, des diapositives, etc. dans le Diagram dans la forme unique avec à la fois des données d'objet et une image d'aperçu à l'intérieur.|Renforcement|
|DIAGRAMNET-51888|Visio en PDF - API prend beaucoup de temps pour la conversion|Renforcement|
|DIAGRAMNET-51889|Enregistrement en pdf en boucle de plus de 20 minutes|Renforcement|
|DIAGRAMNET-51893|Attribut viewBox manquant après la conversion VSDX en SVG|Renforcement|
|DIAGRAMNET-51851|VSDX au format PDF - certaines icônes sont manquantes et certaines ne sont pas rendues correctement|Punaise|
|DIAGRAMNET-51873|VSDX en PDF - Le contenu est à gauche dans le PDF de sortie|Punaise|
|DIAGRAMNET-51874|VSDX en PDF - le contenu et les lignes manquent dans la sortie|Punaise|
|DIAGRAMNET-51876|VSDX en PNG - certaines formes sont incorrectes dans la sortie|Punaise|
|DIAGRAMNET-51879|Visio en PDF - la sortie n'est pas correcte|Punaise|
|DIAGRAMNET-51894|System.NullReferenceException lors du chargement du diagram|Punaise|
|DIAGRAMNET-51895|Impossible de récupérer les données de propriété de groupe telles que SelectionModel, DisplayMode|Punaise|

## **Public API et modifications incompatibles avec les versions antérieures**  ##
Vous trouverez ci-dessous une liste de toutes les modifications apportées au public API, telles que les membres ajoutés, renommés, supprimés ou obsolètes, ainsi que toute modification non rétrocompatible apportée à Aspose.Diagram for .NET. Si vous avez des inquiétudes concernant l'un des changements répertoriés, veuillez le signaler sur le forum d'assistance Aspose.Diagram.

####  Ajout de la méthode AddShape dans la page ####
```
Diagram diagram = new Diagram();

// Get page object by index
Aspose.Diagram.Page page0 = diagram.Pages[0];
// set pinX, pinY, width and height
double pinX = 2, pinY = 2, width = 4, hieght = 3;

// Import ole as Visio shape word
page0.AddShape(pinX, pinY, width, hieght, new FileStream( "imageword.emf", FileMode.OpenOrCreate), new FileStream( "wordsource.doc", FileMode.OpenOrCreate));
```
