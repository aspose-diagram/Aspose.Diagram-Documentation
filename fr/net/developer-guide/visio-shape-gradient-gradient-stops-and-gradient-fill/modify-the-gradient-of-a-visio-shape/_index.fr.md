---
title: Modifier le dégradé d'une forme Visio
type: docs
weight: 10
url: /fr/net/modify-the-gradient-of-a-visio-shape/
description: Cette page décrit comment modifier la couleur du dégradé d'une forme visio avec la bibliothèque Aspose.Diagram.
---
{{% alert color="primary" %}} 

En utilisant Aspose.Diagram API, les développeurs peuvent améliorer l'apparence d'une forme Visio en modifiant les propriétés du dégradé. Les développeurs peuvent récupérer un remplissage dégradé pour définir la direction, l'angle, la couleur et la position d'arrêt du dégradé, etc.

{{% /alert %}} 
## **Modifier l'exemple de programmation de remplissage dégradé**
[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)La classe offre la propriété Fill qui permet aux développeurs de récupérer un[Remplissage en dégradé](http://www.aspose.com/api/net/diagram/aspose.diagram/gradientfill)objet. La classe GradientFill contient les données de dégradé d'une forme Visio. Les développeurs peuvent définir toutes ses propriétés disponibles ainsi que récupérer un arrêt de dégradé par index pour définir les propriétés de couleur et de position.


{{< highlight csharp >}}
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeGradientFillData();
// Load the Visio diagram
Diagram diagram = new Diagram(dataDir + "ShapewithGradientFill.vsdx");
// get page by name
Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");
// get shape by ID
Aspose.Diagram.Shape shape = page.Shapes.GetShape(1);
// get the gradient fill properties
GradientFill gradientfill = shape.Fill.GradientFill;
// get the gradient stops
GradientStopCollection stops = gradientfill.GradientStops;
// get the gradient stop by index
GradientStop stop = stops[0];
// set gradient stop properties
stop.Color.Ufe.F = "";
stop.Position.Value = 0.5;
gradientfill.GradientDir.Value = (int)GradientFillDir.RectangleFromBottomRight;
gradientfill.GradientAngle.Value = 0.7853981633974501;
// save the Visio drawing
diagram.Save(dataDir + "ShapewithGradientFill_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

