---
title: Offentlig API Ändringar i Aspose.Diagram 16.12.0
type: docs
weight: 10
url: /sv/net/public-api-changes-in-aspose-diagram-16-12-0/
---
{{% alert color="primary" %}} 

Det här dokumentet beskriver ändringar av Aspose.Diagram API från version 16.11.0 till 16.12.0, som kan vara av intresse för modul-/applikationsutvecklare. Den innehåller inte bara nya och uppdaterade offentliga metoder, utan också en beskrivning av eventuella förändringar i beteendet bakom kulisserna i Aspose.Diagram.

{{% /alert %}} 
## **Ändra egenskaper för en gradient**
Utvecklare kan hämta ett gradientstopp och sedan ändra dess egenskaper. Vi har lagt till[GradientFill](http://www.aspose.com/api/net/diagram/aspose.diagram/gradientfill)och[GradientStop](http://www.aspose.com/api/net/diagram/aspose.diagram/gradientstop)klasser för detta ändamål. Kontrollera kodexemplet:

**C#**

{{< highlight "csharp" >}}

 // load a Visio drawing

Diagram diagram = new Diagram(@"C:\temp\MyVisio.vsdx");

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

diagram.Save(@"C:\temp\Output.pdf", SaveFileFormat.PDF);

{{< /highlight >}}
