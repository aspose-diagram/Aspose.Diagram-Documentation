---
title: Public API Changements dans Aspose.Diagram 16.12.0
type: docs
weight: 10
url: /fr/java/public-api-changes-in-aspose-diagram-16-12-0/
---
{{% alert color="primary" %}} 

Ce document décrit les modifications apportées au Aspose.Diagram API de la version 16.11.0 à 16.12.0, qui peuvent intéresser les développeurs de modules/applications. Il comprend non seulement des méthodes publiques nouvelles et mises à jour, mais également une description de tout changement de comportement dans les coulisses de Aspose.Diagram.

{{% /alert %}} 
### **Modifier les propriétés d'un dégradé**
Les développeurs peuvent récupérer un arrêt de dégradé puis modifier ses propriétés. Nous avons ajouté[Remplissage en dégradé](https://reference.aspose.com/diagram/java/com.aspose.diagram/gradientfill)et[GradientStop](https://reference.aspose.com/diagram/java/com.aspose.diagram/gradientstop)cours à cet effet. Veuillez vérifier l'exemple de code :

**Java**

{{< highlight "csharp" >}}

 // load a Visio drawing

Diagram diagram = new Diagram("C:\\temp\\MyVisio.vsdx");

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

diagram.save("C:\\temp\\Output.pdf", SaveFileFormat.PDF);

{{< /highlight >}}
