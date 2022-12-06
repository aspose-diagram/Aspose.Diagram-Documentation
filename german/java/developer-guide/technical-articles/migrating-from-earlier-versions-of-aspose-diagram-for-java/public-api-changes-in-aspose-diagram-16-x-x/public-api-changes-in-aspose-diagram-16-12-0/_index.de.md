---
title: Öffentlich API Änderungen in Aspose.Diagram 16.12.0
type: docs
weight: 10
url: /de/java/public-api-changes-in-aspose-diagram-16-12-0/
---
{{% alert color="primary" %}} 

Dieses Dokument beschreibt Änderungen an Aspose.Diagram API von Version 16.11.0 bis 16.12.0, die für Modul-/Anwendungsentwickler von Interesse sein könnten. Es enthält nicht nur neue und aktualisierte öffentliche Methoden, sondern auch eine Beschreibung aller Änderungen im Verhalten hinter den Kulissen in Aspose.Diagram.

{{% /alert %}} 
### **Eigenschaften eines Farbverlaufs ändern**
Entwickler können einen Gradientenstopp abrufen und dann seine Eigenschaften ändern. Wir haben hinzugefügt[GradientFill](https://reference.aspose.com/diagram/java/com.aspose.diagram/gradientfill)und[GradientStop](https://reference.aspose.com/diagram/java/com.aspose.diagram/gradientstop)Klassen zu diesem Zweck. Bitte überprüfen Sie das Codebeispiel:

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
