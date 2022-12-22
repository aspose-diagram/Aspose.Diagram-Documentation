---
title: Öffentlich API Änderungen in Aspose.Diagram 16.12.0
type: docs
weight: 10
url: /de/net/public-api-changes-in-aspose-diagram-16-12-0/
---
{{% alert color="primary" %}} 

Dieses Dokument beschreibt Änderungen an Aspose.Diagram API von Version 16.11.0 bis 16.12.0, die für Modul-/Anwendungsentwickler von Interesse sein könnten. Es enthält nicht nur neue und aktualisierte öffentliche Methoden, sondern auch eine Beschreibung aller Änderungen im Verhalten hinter den Kulissen in Aspose.Diagram.

{{% /alert %}} 
## **Eigenschaften eines Farbverlaufs ändern**
Entwickler können einen Gradientenstopp abrufen und dann seine Eigenschaften ändern. Wir haben hinzugefügt[GradientFill](http://www.aspose.com/api/net/diagram/aspose.diagram/gradientfill)und[GradientStop](http://www.aspose.com/api/net/diagram/aspose.diagram/gradientstop)Klassen zu diesem Zweck. Bitte überprüfen Sie das Codebeispiel:

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
