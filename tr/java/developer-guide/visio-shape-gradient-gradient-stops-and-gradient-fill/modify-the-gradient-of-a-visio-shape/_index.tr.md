---
title: Visio Şeklinin Degradesini Değiştirme
type: docs
weight: 10
url: /tr/java/modify-the-gradient-of-a-visio-shape/
---
{{% alert color="primary" %}} 

Aspose.Diagram API'i kullanan geliştiriciler, degradenin özelliklerini değiştirerek bir Visio şeklinin görünümünü iyileştirebilir. Geliştiriciler, yönü, açıyı, gradyan durdurma rengini ve konumunu vb. ayarlamak için bir gradyan dolgusu alabilir.

{{% /alert %}} 
## **Degrade Doldurma Programlama Örneğinin Değiştirilmesi**
[Şekil](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)class, geliştiricilerin bir[Gradyan Doldurma](https://reference.aspose.com/diagram/java/com.aspose.diagram/gradientfill)nesne. GradientFill sınıfı, bir Visio Shape'in gradyan verilerini tutar. Geliştiriciler, mevcut tüm özelliklerini ayarlayabilir ve renk ve konum özelliklerini ayarlamak için dizine göre bir gradyan durağı alabilir.

```
{{< highlight "java" >}}
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(ModifyShapeGradientFill.class) + "ShapeGradientFill\\";

// load a Visio drawing
Diagram diagram = new Diagram(dataDir + "ShapewithGradientFill.vsdx");
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
diagram.save(dataDir + "ShapewithGradientFill_out.vsdx", SaveFileFormat.VSDX);
{{< /highlight >}}
```
