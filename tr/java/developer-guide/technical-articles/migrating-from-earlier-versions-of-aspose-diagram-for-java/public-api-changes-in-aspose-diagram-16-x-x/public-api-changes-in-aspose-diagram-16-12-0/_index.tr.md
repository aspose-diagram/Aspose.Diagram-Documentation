---
title: Genel API Aspose.Diagram 16.12.0'daki değişiklikler
type: docs
weight: 10
url: /tr/java/public-api-changes-in-aspose-diagram-16-12-0/
---
{{% alert color="primary" %}} 

Bu belge, modül/uygulama geliştiricilerinin ilgisini çekebilecek 16.11.0 sürümünden 16.12.0 sürümüne Aspose.Diagram API değişikliklerini açıklamaktadır. Yalnızca yeni ve güncellenmiş genel yöntemleri değil, aynı zamanda Aspose.Diagram'deki perde arkasındaki davranışlardaki değişikliklerin açıklamasını da içerir.

{{% /alert %}} 
### **Degradenin Özelliklerini Değiştirme**
Geliştiriciler bir degrade durağını alabilir ve ardından özelliklerini değiştirebilir. Biz ekledik[Gradyan Doldurma](https://reference.aspose.com/diagram/java/com.aspose.diagram/gradientfill)ve[Gradyan Durdurma](https://reference.aspose.com/diagram/java/com.aspose.diagram/gradientstop)Bu amaçlar için sınıflar. Lütfen kod örneğini kontrol edin:

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
