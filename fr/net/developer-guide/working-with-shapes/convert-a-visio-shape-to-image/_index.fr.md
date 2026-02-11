---
title: Convertir une forme Visio en image
type: docs
weight: 10
url: /fr/net/convert-a-visio-shape-to-image/
description: Cette section explique comment convertir une forme visio en image avec Aspose.Diagram.
---
## **Convertir une forme visio en image**
Cette rubrique explique comment les développeurs peuvent convertir une forme visio en image à l'aide de Aspose.Diagram.
 La méthode ToImage exposée par le[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class peut être utilisé pour convertir en image.


Le code ci-dessous montre comment :

1. Charger un échantillon diagram.
1. obtenir une page particulière.
1. obtenir une forme particulière.
1. convertir la forme en image.
#### **Exemple de programmation de la forme à l'image**
Utilisez le code suivant dans votre application .net pour convertir une forme visio en image.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToImage.vsdx");

// Get a particular page
Page page = diagram.Pages[0];

// Get a particular shape
Shape shape = page.Shapes[0];

// Shape to Image
Aspose.Diagram.Saving.ImageSaveOptions o = new Aspose.Diagram.Saving.ImageSaveOptions(SaveFileFormat.PNG);
shape.ToImage("out.png", o);

{{< /highlight >}}

