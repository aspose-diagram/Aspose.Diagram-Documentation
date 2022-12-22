---
title: Aspose.Diagram for .NET 19.1 Release Notes
type: docs
weight: 120
url: /sv/net/aspose-diagram-for-net-19-1-release-notes/
---
{{% alert color="primary" %}} 

Den här sidan innehåller release notes för[Aspose.Diagram for .NET 19.1](https://www.nuget.org/packages/Aspose.Diagram/19.1.0)

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-51082|Lägg till stöd för att rita Polyline|Förbättring|
|DIAGRAMNET-51084|Lägg till stöd för att rita Bezier-former|Förbättring|
|DIAGRAMNET-51231|Återge kommentarer när du sparar som bild eller HTML|Förbättring|
|DIAGRAMNET-51597| VISIO till SVG - Använd rektangulära element<path> tagga istället för<Rect>|Förbättring|
|DIAGRAMNET-50764|VSDX läsning saknar färgvärdet för olika former|Insekt|
|DIAGRAMNET-51336|Åtgärda problem i versionen Aspose.Diagram for .NET/Java|Insekt|
|DIAGRAMNET-51343|Utdata VSDX - formstorleken ändras inte|Insekt|
|DIAGRAMNET-51579|Läslås som finns efter att metoden Save() anropas|Insekt|
## **Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över eventuella ändringar som gjorts för allmänheten API, t.ex. tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for .NET. Om du har frågor om någon ändring i listan, vänligen ta upp dem i de[Aspose.Diagram supportforum](https://forum.aspose.com/c/diagram/17).
### **Lägger till DrawPolyline på sidan**
Processen att rita polylinje.

{{< highlight "java" >}}

 PointF[]ps = new PointF[]{new PointF(1, 1), new PointF(2, 2), new PointF(3.79949292203676f, 0) };

diagram.Pages[0].DrawPolyline(1, 1, 2, 2, ps);

{{< /highlight >}}
### **Lägger till DrawBezier på sidan**
Processen att rita bezier.

{{< highlight "java" >}}

 PointF[]ps = new PointF[]{new PointF(1, 1), new PointF(2, 2)};

diagram.Pages[0].DrawBezier(1, 1, 2, 2, ps);

{{< /highlight >}}
### **Lägger till IsExportComments i ImageSaveOptions och HTMLSaveOptions**
Definierar om kommentarerna behöver exporteras eller inte.

{{< highlight "java" >}}

 Aspose.Diagram.Saving.ImageSaveOptions io = new Aspose.Diagram.Saving.ImageSaveOptions(SaveFileFormat.PNG);

io.IsExportComments = true;

Aspose.Diagram.Saving.HTMLSaveOptions htmlo = new Aspose.Diagram.Saving.HTMLSaveOptions();

htmlo.IsExportComments = false;

{{< /highlight >}}
### **Lägger till ExportElementAsRectTag i SVGSaveOptions**
Definierar om rektangelelement behöver exporteras som rect-tagg eller inte.

{{< highlight "java" >}}

 var SVGso = new Aspose.Diagram.Saving.SVGSaveOptions();

SVGso.ExportGuideShapes = false;

SVGso.SaveFormat = Aspose.Diagram.SaveFileFormat.SVG;

SVGso.SVGFitToViewPort = true;

SVGso.ExportElementAsRectTag = true;

{{< /highlight >}}
