---
title: Convertir une forme Visio en Svg
type: docs
weight: 10
url: /fr/net/convert-a-visio-shape-to-svg/
description: Cette section explique comment convertir une forme visio en svg avec Aspose.Diagram.
---
## ** Convertir une forme visio en svg**
 La méthode ToSvg exposée par le[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) la classe peut être utilisée pour convertir en svg.

Le code ci-dessous montre comment :

1. Charger un échantillon diagram.
1. obtenir une page particulière.
1. obtenir une forme particulière.
1. convertir la forme en svg.
### **Forme en Svg**
Utilisez le code suivant dans votre application .net pour convertir une forme visio en svg.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToSvg.vsdx");

// Get a particular page
Page page = diagram.Pages[0];

// Get a particular shape
Shape shape = page.Shapes[0];

SVGSaveOptions svgOptions = new SVGSaveOptions();
// Shape to Svg
shape.ToSvg("out.svg",svgOptions);

{{< /highlight >}}


