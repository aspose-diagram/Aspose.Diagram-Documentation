---
title: Aspose.Diagram for .NET 17.9 Release Notes
type: docs
weight: 40
url: /sv/net/aspose-diagram-for-net-17-9-release-notes/
---
{{% alert color="primary" %}} 

 Den här sidan innehåller release notes för[Aspose.Diagram for .NET 17.9](https://www.nuget.org/packages/Aspose.Diagram/17.9.0).

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-51261|Lägg till stöd för att konvertera det specifika området på en ritning till bild|Förbättring|
|DIAGRAMNET-51350|Lägg till stöd för att hämta form efter namn|Förbättring|
|DIAGRAMNET-51351|Lägg till stöd för att hämta formen från Annotation|Förbättring|
|DIAGRAMNET-51295|VSDX till SVG - den låga kvaliteten på SVG-utdata|Insekt|
|DIAGRAMNET-51309|DiagramException inträffar vid VSDX filsparande|Insekt|
|DIAGRAMNET-51331|VSDM till SVG - textobjekten flyttas upp|Insekt|
|DIAGRAMNET-51333|VSDM till SVG - felaktig återgivning av de cirkulära ikonerna|Insekt|
|DIAGRAMNET-51339|VSDX till SVG - trunkeringen av text från höger sida av varje bild|Insekt|
|DIAGRAMNET-51340|Felaktig kommentarsordning|Insekt|
|` `DIAGRAMNET-51342|Minnet är slut efter att ha använt "AddComment"-metoden och sparat filen på steam|Insekt|
|DIAGRAMNET-51344|VSDX till PDF - ett argument utanför intervallet fel inträffade|Insekt|
|DIAGRAMNET-51345|Kommentaren raderas inte tillsammans med formen|Insekt|
|DIAGRAMNET-51346|VSDM till SVG - logotypens kvalitet är nedgraderad|Insekt|
|DIAGRAMNET-51347|VSDM till SVG - logotypens kvalitet är nedgraderad|Insekt|
|DIAGRAMNET-51353|Det går inte att lägga till ytterligare en kommentar på sidan Visio|Insekt|
|DIAGRAMNET-51354|Det går inte att redigera kommentarer på sidan Visio|Insekt|
## **Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över eventuella ändringar som gjorts för allmänheten API, t.ex. tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for .NET. Om du har frågor om någon ändring i listan, vänligen ta upp dem i de[Aspose.Diagram supportforum](https://forum.aspose.com/c/diagram/17).
### **Lägger till GetShape-medlem i ShapeCollection**
Det gör det möjligt att hämta en form efter namn.

{{< highlight "java" >}}

 string dataDir = @"C:\temp\";

// load a drawing

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// retrieve page by name

Page page = diagram.Pages.GetPage("Page-1");

// retrieve shape by name

Shape shape = page.Shapes.GetShape("name");

{{< /highlight >}}
### **Lägger till ShapeID-medlem i Annotation**
Det gör det möjligt att spåra kommentarens form.

{{< highlight "java" >}}

 string dataDir = @"C:\temp\";

// load a drawing

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get the annotation by index

Annotation annotation = diagram.Pages.GetPage("Page-1").PageSheet.Annotations[1];

// get shape Id

Console.WriteLine(annotation.ShapeID);

{{< /highlight >}}
### **Lägger till område i RenderingSaveOptions**
Det gör det möjligt att konvertera det specifika rektangelområdet i Visio-ritningen.

{{< highlight "java" >}}

 // load a Visio drawing

Diagram diagram = new Diagram(@"c:\\test.vsdx");

ImageSaveOptions Options = new ImageSaveOptions(SaveFileFormat.PNG);

// specify region

Options.Area = new RectangleF(0, 0, 1, 1);

// save into the image format

diagram.Save("e:\\area.png", Options);

{{< /highlight >}}
### **Användningsexempel**
Kontrollera listan med hjälpämnen som lagts till i Aspose.Diagram Wiki-dokument:

1. [Konvertera specificerat område på Visio-sidan till en bild](https://docs.aspose.com/diagram/net/working-with-images/#convert-specified-area-of-the-visio-page-to-an-image)
1. [Placera automatiskt en samling former på sidan Visio](/diagram/sv/net/auto-space-a-collection-of-shapes-in-the-visio-page/)
