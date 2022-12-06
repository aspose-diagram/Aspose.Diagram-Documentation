---
title: Aspose.Diagram for .NET 18.11 Notes de mise à jour
type: docs
weight: 20
url: /fr/net/aspose-diagram-for-net-18-11-release-notes/
---
{{% alert color="primary" %}} 

Cette page contient des notes de version pour[Aspose.Diagram for .NET 18.11](https://www.nuget.org/packages/Aspose.Diagram/18.11.0)

{{% /alert %}} 
## **Améliorations et changements**

|**Clé**|**Sommaire**|**Catégorie**|
|:- |:- |:- |
|DIAGRAMNET-50410|MilestoneHelper - Ajout de la prise en charge du paramètre de format de chaîne de date personnalisé|Renforcement|
|DIAGRAMNET-51568|Ajouter une option pour définir ViewBox dans SaveOptions pour SVG|Renforcement|
|DIAGRAMNET-51580|Aspose.Diagram crée SVG avec des directives et MS Visio ne le fait pas|Renforcement|
|DIAGRAMNET-51556|La méthode Shape.ToImage ne génère pas d'images correctes|Punaise|
|DIAGRAMNET-51557|La méthode Shape.ToImage renvoie des images vierges en cas de copie de la page|Punaise|
|DIAGRAMNET-51570|La méthode Shape.ToImage ne génère pas d'images correctes|Punaise|
|DIAGRAMNET-51576|VSDX en PDF - Blocs de texte manquants|Punaise|
|DIAGRAMNET-51578|VSDX pour afficher les résultats dans StackOverFlowException|Punaise|
## **Public API et modifications incompatibles avec les versions antérieures**
Voici une liste de toutes les modifications apportées au public API, telles que les membres ajoutés, renommés, supprimés ou obsolètes, ainsi que toute modification non rétrocompatible apportée à Aspose.Diagram for .NET. Si vous avez des préoccupations concernant l'un des changements répertoriés, veuillez les signaler dans la[Aspose.Diagram forum d'assistance](https://forum.aspose.com/c/diagram/17).
### **Ajoute SVGFitToViewPort dans SVGSaveOptions**
Si cette propriété est vraie, le SVG généré s'adaptera au port d'affichage.

{{< highlight "java" >}}

 SVGSaveOptions option = new SVGSaveOptions();

option.SVGFitToViewPort = true;

SVGSaveOptions option = new SVGSaveOptions();

option.SVGFitToViewPort = true;

{{< /highlight >}}
### **Ajoute ExportGuideShapes dans RenderingSaveOptions**
Définit s'il est nécessaire ou non d'exporter les formes de guidage.

{{< highlight "java" >}}

 Aspose.Diagram.Saving.SVGSaveOptions o = new SVGSaveOptions();

o.ExportGuideShapes = false;

{{< /highlight >}}
### **Ajoute DateFormatString dans MilestoneHelper**
DateFormat chaîne de forme

{{< highlight "java" >}}

 milestoneHelper.DateFormatString = "yyyy/mm/dd";

{{< /highlight >}}
