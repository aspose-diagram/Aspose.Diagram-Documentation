---
title: Público API Cambios en Aspose.Diagram 16.12.0
type: docs
weight: 10
url: /es/net/public-api-changes-in-aspose-diagram-16-12-0/
---
{{% alert color="primary" %}} 

Este documento describe los cambios al Aspose.Diagram API de la versión 16.11.0 a la 16.12.0, que pueden ser de interés para los desarrolladores de módulos/aplicaciones. Incluye no solo métodos públicos nuevos y actualizados, sino también una descripción de cualquier cambio en el comportamiento detrás de escena en Aspose.Diagram.

{{% /alert %}} 
## **Modificar propiedades de un degradado**
Los desarrolladores pueden recuperar una parada de gradiente y luego modificar sus propiedades. hemos añadido[Relleno degradado](http://www.aspose.com/api/net/diagram/aspose.diagram/gradientfill)y[GradienteParada](http://www.aspose.com/api/net/diagram/aspose.diagram/gradientstop)clases para este fin. Por favor, compruebe el ejemplo de código:

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
