---
title: Aspose.Diagram for .NET 17.8 Notes de mise à jour
type: docs
weight: 50
url: /fr/net/aspose-diagram-for-net-17-8-release-notes/
---
{{% alert color="primary" %}} 

 Cette page contient des notes de version pour[Aspose.Diagram for .NET 17.8](https://www.nuget.org/packages/Aspose.Diagram/17.8.0).

{{% /alert %}} 
## **Améliorations et changements**

|**Clé**|**Sommaire**|**Catégorie**|
|:- |:- |:- |
|DIAGRAMNET-51295|VSDX en SVG - la faible qualité de la sortie SVG.|Renforcement|
|DIAGRAMNET-51298|SVGSaveOptions - ajoute le support pour contrôler le niveau de compression bitmap.|Renforcement|
|DIAGRAMNET-51300|Ajout de la prise en charge des formes de connexion avec index de connexion.|Renforcement|
|DIAGRAMNET-50577|VSDX en conversion PDF, le texte de la forme circulaire est mal placé - I.|Punaise|
|DIAGRAMNET-50582|VSDX en conversion HTML, le texte de la forme circulaire est mal placé - I.|Punaise|
|DIAGRAMNET-50601|VSDX en conversion PDF, le texte de la forme circulaire est mal placé - II.|Punaise|
|DIAGRAMNET-50606|VSDX à la conversion HTML, le texte de la forme circulaire est mal placé - II.|Punaise|
|DIAGRAMNET-51197|Les formes de triangle d'avertissement ne sont pas rendues correctement lors de l'enregistrement de VSDM au format SVG.|Punaise|
|DIAGRAMNET-51245|Éléments de texte déplacés lors de la conversion d'un VSD en PDF.|Punaise|
|DIAGRAMNET-51246|Polices incorrectes appliquées au texte lors de la conversion d'un VSD en PDF.|Punaise|
|DIAGRAMNET-51296|VSDM en SVG - l'image est tronquée.|Punaise|
|DIAGRAMNET-51301|VSDX en PDF - la couleur du texte sur les lignes de connexion est modifiée.|Punaise|
|DIAGRAMNET-51302|VSDX au format PDF - éléments graphiques manquants.|Punaise|
|DIAGRAMNET-51304|VSDX au format PDF - rendu incomplet de l'organigramme.|Punaise|
|DIAGRAMNET-51305|VSDX au format PDF - éléments graphiques manquants.|Punaise|
|DIAGRAMNET-51306|VSDX en PDF - la couleur du texte sur les lignes de connexion est modifiée.|Punaise|
|DIAGRAMNET-51307|VSDX au format PDF - éléments graphiques manquants.|Punaise|
|DIAGRAMNET-51313|La routine d'ouverture et de sauvegarde d'un dessin VSDX génère un fichier de sortie corrompu.|Punaise|
|DIAGRAMNET-51314|VSDX en SVG - positionnement incorrect du texte.|Punaise|
|DIAGRAMNET-51317|VSDX au format PDF - le texte des lignes de connexion est manquant.|Punaise|
|DIAGRAMNET-51318|VSDX au format PDF - le texte en gras des formes rectangulaires est manquant.|Punaise|
|DIAGRAMNET-51319|VSDM à SVG - l'opération arithmétique a entraîné une erreur de débordement.|Punaise|
|DIAGRAMNET-51320|Erreur dans l'élément de forme lors du chargement d'un VSDM.|Punaise|
|DIAGRAMNET-51323|VSDM à SVG - toutes les lignes de connexion sont manquantes.|Punaise|
|DIAGRAMNET-51324|VSDM à SVG - style de bordure incorrect et couleur de bordure de différentes formes.|Punaise|
|DIAGRAMNET-51326|Problème après l'ajout de deux commentaires à la forme.|Punaise|
|DIAGRAMNET-51327|Problème après l'utilisation de la méthode "AddComment" lors de l'ajout de commentaires à diverses formes.|Punaise|
|DIAGRAMNET-51328|Aspose Diagram importe incorrectement la forme dans le document.|Punaise|
|DIAGRAMNET-51330|VSDM en SVG - un texte de filigrane supplémentaire est ajouté.|Punaise|
|DIAGRAMNET-51332|VSDM en SVG - rendu incorrect d'une icône.|Punaise|
|DIAGRAMNET-51334|VSDM en SVG - texte déplacé dans le coin supérieur droit.|Punaise|
|DIAGRAMNET-51335|VSDM en SVG - rendu incorrect de l'image d'arrière-plan.|Punaise|
|DIAGRAMNET-51337|VSD en HTML - format non valide de l'erreur de chaîne d'entrée.|Punaise|
## **Public API et modifications incompatibles avec les versions antérieures**
Voici une liste de toutes les modifications apportées au public API, telles que les membres ajoutés, renommés, supprimés ou obsolètes, ainsi que toute modification non rétrocompatible apportée à Aspose.Diagram for .NET. Si vous avez des préoccupations concernant l'un des changements répertoriés, veuillez les signaler dans la[Aspose.Diagram forum d'assistance](https://forum.aspose.com/c/diagram/17).
### **Ajoute un membre Quality dans la classe SVGSaveOptions**
Il obtient ou définit une valeur déterminant la qualité des images générées.

{{< highlight "java" >}}

 string dataDir = @"c:\temp\";

// Load an existing drawing

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// specify SVG export settings

SVGSaveOptions options = new SVGSaveOptions();

// set image quality

options.Quality = 100;

// save drawing in the SVG format

diagram.Save(dataDir + "UseSVGSaveOptions_out.svg", options);

{{< /highlight >}}
### **Ajoute la méthode ConnectShapesViaConnectorIndex dans la classe Page**
Il permet de connecter des formes à l'aide d'index de connexion.

{{< highlight "java" >}}

 string dataDir = @"c:\temp\";

// Load an existing drawing

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get shapes by ID

Aspose.Diagram.Shape shape1 = diagram.Pages[0].Shapes.GetShape(1);

Aspose.Diagram.Shape shape2 = diagram.Pages[0].Shapes.GetShape(2);

// add connector shapes

Aspose.Diagram.Shape connector1 = new Aspose.Diagram.Shape();

long connecter1Id = diagram.AddShape(connector1, "Dynamic connector", 0);

// connect shapes by index of conneecting points

diagram.Pages[0].ConnectShapesViaConnectorIndex(shape1.ID, 6, shape2.ID, 3, connecter1Id);

// save drawing

diagram.Save(dataDir + "UseSVGSaveOptions_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **Exemples d'utilisation**
Veuillez consulter la liste des rubriques d'aide ajoutées dans les documents Wiki Aspose.Diagram :

1. [Utiliser les index de connexion pour connecter des formes](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/#use-connection-indexes-to-connect-shapes)
1. [Utilisation des options d'enregistrement SVG](https://docs.aspose.com/diagram/net/save-visio-document/)
