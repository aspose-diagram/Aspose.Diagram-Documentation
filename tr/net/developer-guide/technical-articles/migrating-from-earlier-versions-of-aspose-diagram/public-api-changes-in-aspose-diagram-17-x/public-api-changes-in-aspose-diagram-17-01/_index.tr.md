---
title: Kamu API Değişiklikler Aspose.Diagram 17.01
type: docs
weight: 10
url: /tr/net/public-api-changes-in-aspose-diagram-17-01/
---
{{% alert color="primary" %}} 

Bu belge, modül/uygulama geliştiricilerinin ilgisini çekebilecek 16.12.0 sürümünden 17.1.0 sürümüne Aspose.Diagram API değişikliklerini açıklamaktadır. Yalnızca yeni ve güncellenmiş genel yöntemleri değil, aynı zamanda Aspose.Diagram'deki perde arkasındaki davranışlardaki değişikliklerin açıklamasını da içerir.

{{% /alert %}} 
## **Dönüştür Visio Seçici Şekillerle Çizim**
Geliştiriciler, Visio çizimini desteklenen herhangi bir formata dönüştürmek için belirli şekilleri seçebilir. Biz ekledik[şekiller](http://www.aspose.com/api/net/diagram/aspose.diagram.saving/renderingsaveoptions/properties/shapes)üye[RenderingSaveOptions](http://www.aspose.com/api/net/diagram/aspose.diagram.saving/renderingsaveoptions)Bu amaçla sınıf. Her kaydetme seçeneği sınıfı, RenderingSaveOptions sınıfının genişletilmiş biçimidir. Lütfen kod örneğini kontrol edin:

**C#**

{{< highlight "csharp" >}}

 // the path to the documents directory.

string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// call the diagram constructor to load diagram from a VSD file

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// create an instance SVG save options class

SVGSaveOptions options = new SVGSaveOptions();

ShapeCollection shapes = options.Shapes;

// get shapes by page index and shape ID, and then add in the shape collection object

shapes.Add(diagram.Pages[0].Shapes.GetShape(1));

shapes.Add(diagram.Pages[0].Shapes.GetShape(2));

// save Visio drawing

diagram.Save(dataDir + "SelectiveShapes_out.svg", options);

{{< /highlight >}}
