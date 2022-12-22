---
title: Kamu API Değişiklikler Aspose.Diagram 17.01
type: docs
weight: 10
url: /tr/java/public-api-changes-in-aspose-diagram-17-01/
---
{{% alert color="primary" %}} 

Bu belge, Aspose.Diagram API sürümünde 16.12.0'dan 17.01'e modül/uygulama geliştiricilerinin ilgisini çekebilecek değişiklikleri açıklamaktadır. Yalnızca yeni ve güncellenmiş genel yöntemleri değil, aynı zamanda Aspose.Diagram'deki perde arkasındaki davranışlardaki değişikliklerin açıklamasını da içerir.

{{% /alert %}} 
### **Dönüştür Visio Seçici Şekillerle Çizim**
Geliştiriciler, Visio çizimini desteklenen herhangi bir formata dönüştürmek için belirli şekilleri seçebilir. Bu amaçla RenderingSaveOptions sınıfına Shapes üyesini ekledik. Her kaydetme seçeneği sınıfı, RenderingSaveOptions sınıfının genişletilmiş biçimidir. Lütfen kod örneğini kontrol edin:

**Java**

{{< highlight "csharp" >}}

 // The path to the documents directory.

String dataDir = Utils.getSharedDataDir(ConvertVisioWithSelectiveShapes.class) + "LoadSaveConvert\\";

// call the diagram constructor to load diagram from a VSD file

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// create an instance SVG save options class

SVGSaveOptions options = new SVGSaveOptions();

ShapeCollection shapes = options.getShapes();

// get shapes by page index and shape ID, and then add in the shape collection object

shapes.add(diagram.getPages().get(0).getShapes().getShape(1));

shapes.add(diagram.getPages().get(0).getShapes().getShape(2));

// save Visio drawing

diagram.save(dataDir + "SelectiveShapes_out.svg", options);

{{< /highlight >}}
