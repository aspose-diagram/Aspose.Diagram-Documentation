---
title: Modifier le dégradé d'une forme Visio
type: docs
weight: 10
url: /fr/java/modify-the-gradient-of-a-visio-shape/
---
{{% alert color="primary" %}} 

En utilisant Aspose.Diagram API, les développeurs peuvent améliorer l'apparence d'une forme Visio en modifiant les propriétés du dégradé. Les développeurs peuvent récupérer un remplissage dégradé pour définir la direction, l'angle, la couleur et la position d'arrêt du dégradé, etc.

{{% /alert %}} 
## **Modifier l'exemple de programmation de remplissage dégradé**
[Forme](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)La classe offre la propriété Fill qui permet aux développeurs de récupérer un[Remplissage en dégradé](https://reference.aspose.com/diagram/java/com.aspose.diagram/gradientfill)objet. La classe GradientFill contient les données de dégradé d'une forme Visio. Les développeurs peuvent définir toutes ses propriétés disponibles ainsi que récupérer un arrêt de dégradé par index pour définir les propriétés de couleur et de position.


{{< highlight java >}}
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(ModifyShapeGradientFill.class) + "ShapeGradientFill\\";

// load a Visio drawing
Diagram diagram = new Diagram(dataDir + "ShapewithGradientFill.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");
// get shape by ID
Shape shape = page.getShapes().getShape(1);
// get the gradient fill properties
GradientFill gradientfill = shape.getFill().getGradientFill();
// get the gradient stops
GradientStopCollection stops = gradientfill.getGradientStops();
// get the gradient stop by index
GradientStop stop = stops.get(0);
// set gradient stop properties
stop.getColor().getUfe().setF("");
stop.getPosition().setValue(0.5);
gradientfill.getGradientDir().setValue(GradientFillDir.RECTANGLE_FROM_BOTTOM_RIGHT);
gradientfill.getGradientAngle().setValue(0.7853981633974501);
// save the Visio drawing
diagram.save(dataDir + "ShapewithGradientFill_out.vsdx", SaveFileFormat.VSDX);
{{< /highlight >}}

