---
title: Pubblico API Modifiche Aspose.Diagram 16.12.0
type: docs
weight: 10
url: /it/net/public-api-changes-in-aspose-diagram-16-12-0/
---
{{% alert color="primary" %}} 

Questo documento descrive le modifiche allo Aspose.Diagram API dalla versione 16.11.0 alla 16.12.0, che potrebbero interessare gli sviluppatori di moduli/applicazioni. Include non solo metodi pubblici nuovi e aggiornati, ma anche una descrizione di eventuali cambiamenti nel comportamento dietro le quinte in Aspose.Diagram.

{{% /alert %}} 
## **Modifica le proprietà di un gradiente**
Gli sviluppatori possono recuperare un'interruzione del gradiente e quindi modificarne le proprietà. Abbiamo aggiunto[GradientFill](http://www.aspose.com/api/net/diagram/aspose.diagram/gradientfill)e[GradientStop](http://www.aspose.com/api/net/diagram/aspose.diagram/gradientstop)classi per questo scopo. Si prega di controllare l'esempio di codice:

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
