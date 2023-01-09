---
title: Public API Changements dans Aspose.Diagram 17,01
type: docs
weight: 10
url: /fr/net/public-api-changes-in-aspose-diagram-17-01/
---
{{% alert color="primary" %}} 

Ce document décrit les modifications apportées au Aspose.Diagram API de la version 16.12.0 à 17.1.0, qui peuvent intéresser les développeurs de modules/applications. Il comprend non seulement des méthodes publiques nouvelles et mises à jour, mais également une description de tout changement de comportement dans les coulisses de Aspose.Diagram.

{{% /alert %}} 
## **Convertir le dessin Visio avec des formes sélectives**
Les développeurs peuvent sélectionner des formes spécifiques pour convertir le dessin Visio en tout autre format pris en charge. Nous avons ajouté[Formes](http://www.aspose.com/api/net/diagram/aspose.diagram.saving/renderingsaveoptions/properties/shapes)membre dans le[RenderingSaveOptions](http://www.aspose.com/api/net/diagram/aspose.diagram.saving/renderingsaveoptions)classe à cet effet. Chaque classe d'options de sauvegarde est la forme étendue de la classe RenderingSaveOptions. Veuillez vérifier l'exemple de code :

**C#**

{{< highlight "csharp" >}}

 // the path to the documents directory.

string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// call the diagram constructor to load diagram from a VSD file

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// create an instance SVG save options class

SVGSaveOptions options = new SVGSaveOptions();

ShapeCollection shapes = options.Shapes;

// get shapes by page index and shape ID, and then add in the shape collection object

shapes.Add(diagram.Pages[0].Shapes.GetShape(1));

shapes.Add(diagram.Pages[0].Shapes.GetShape(2));

// save Visio drawing

diagram.Save(dataDir + "SelectiveShapes_out.svg", options);

{{< /highlight >}}
