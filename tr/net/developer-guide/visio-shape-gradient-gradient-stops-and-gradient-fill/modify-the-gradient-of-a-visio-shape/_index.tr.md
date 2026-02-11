---
title: Visio Şeklinin Degradesini Değiştirme
type: docs
weight: 10
url: /tr/net/modify-the-gradient-of-a-visio-shape/
description: Bu sayfada, visio şeklinin gradyan renginin Aspose.Diagram kitaplığıyla nasıl değiştirileceği açıklanmaktadır.
---
{{% alert color="primary" %}} 

Aspose.Diagram API'i kullanan geliştiriciler, degradenin özelliklerini değiştirerek bir Visio şeklinin görünümünü iyileştirebilir. Geliştiriciler, yönü, açıyı, gradyan durdurma rengini ve konumunu vb. ayarlamak için bir gradyan dolgusu alabilir.

{{% /alert %}} 
## **Degrade Doldurma Programlama Örneğinin Değiştirilmesi**
[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)class, geliştiricilerin bir[Gradyan Doldurma](http://www.aspose.com/api/net/diagram/aspose.diagram/gradientfill)nesne. GradientFill sınıfı, bir Visio Shape'in gradyan verilerini tutar. Geliştiriciler, mevcut tüm özelliklerini ayarlayabilir ve renk ve konum özelliklerini ayarlamak için dizine göre bir gradyan durağı alabilir.


{{< highlight csharp >}}
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeGradientFillData();
// Load the Visio diagram
Diagram diagram = new Diagram(dataDir + "ShapewithGradientFill.vsdx");
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
diagram.Save(dataDir + "ShapewithGradientFill_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

