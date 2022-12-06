---
title: Genel API Aspose.Diagram 16.12.0'daki değişiklikler
type: docs
weight: 10
url: /tr/net/public-api-changes-in-aspose-diagram-16-12-0/
---
{{% alert color="primary" %}} 

Bu belge, modül/uygulama geliştiricilerinin ilgisini çekebilecek 16.11.0 sürümünden 16.12.0 sürümüne Aspose.Diagram API değişikliklerini açıklamaktadır. Yalnızca yeni ve güncellenmiş genel yöntemleri değil, aynı zamanda Aspose.Diagram'deki perde arkasındaki davranışlardaki değişikliklerin açıklamasını da içerir.

{{% /alert %}} 
## **Degradenin Özelliklerini Değiştirme**
Geliştiriciler bir degrade durağını alabilir ve ardından özelliklerini değiştirebilir. Biz ekledik[Gradyan Doldurma](http://www.aspose.com/api/net/diagram/aspose.diagram/gradientfill)ve[Gradyan Durdurma](http://www.aspose.com/api/net/diagram/aspose.diagram/gradientstop)Bu amaçlar için sınıflar. Lütfen kod örneğini kontrol edin:

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
