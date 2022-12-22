---
title: Offentlig API Ändringar i Aspose.Diagram 16.12.0
type: docs
weight: 10
url: /sv/java/public-api-changes-in-aspose-diagram-16-12-0/
---
{{% alert color="primary" %}} 

Det här dokumentet beskriver ändringar av Aspose.Diagram API från version 16.11.0 till 16.12.0, som kan vara av intresse för modul-/applikationsutvecklare. Den innehåller inte bara nya och uppdaterade offentliga metoder, utan också en beskrivning av eventuella förändringar i beteendet bakom kulisserna i Aspose.Diagram.

{{% /alert %}} 
### **Ändra egenskaper för en gradient**
Utvecklare kan hämta ett gradientstopp och sedan ändra dess egenskaper. Vi har lagt till[GradientFill](https://reference.aspose.com/diagram/java/com.aspose.diagram/gradientfill)och[GradientStop](https://reference.aspose.com/diagram/java/com.aspose.diagram/gradientstop)klasser för detta ändamål. Kontrollera kodexemplet:

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
