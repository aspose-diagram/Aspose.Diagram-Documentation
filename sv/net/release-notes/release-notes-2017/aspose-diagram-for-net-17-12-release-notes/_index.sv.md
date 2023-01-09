---
title: Aspose.Diagram for .NET 17.12 Release Notes
type: docs
weight: 10
url: /sv/net/aspose-diagram-for-net-17-12-release-notes/
---
{{% alert color="primary" %}} 

 Den här sidan innehåller release notes för[Aspose.Diagram for .NET 17.12](https://www.nuget.org/packages/Aspose.Diagram/17.12.0).

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-50016|Lägg till stöd för att duplicera/klona en form|Förbättring|
|DIAGRAMNET-50677|Ange singeln API för att konvertera en Visio-form till PDF|Förbättring|
|DIAGRAMNET-50678|Ange singeln API för att konvertera en Visio-form till HTML|Förbättring|
|DIAGRAMNET-50762|Parsningsfelet för det långa attributvärdet inträffade när en VDX diagram genererades|Insekt|
|DIAGRAMNET-51401|Utdata VSDX - kontrollerna i Shapes fungerar inte|Insekt|
|DIAGRAMNET-51402|VSDX till bild - ett OLE-objekt bevaras inte|Insekt|
|DIAGRAMNET-51406|VSD till bild - de extra tecknen visas|Insekt|
|DIAGRAMNET-51410|VSD till PDF - sidnumret förblir 4 på alla sidor|Insekt|
|DIAGRAMNET-51411|VSD till bild - sidnumret förblir 4 på alla sidor|Insekt|
|DIAGRAMNET-51414|VSDX till PDF - saknar innehållet i former|Insekt|
|DIAGRAMNET-51415|VSDX till PDF - felaktig bakgrundsfärg på formerna|Insekt|
|DIAGRAMNET-51416|VSDX till HTML - felaktig bakgrundsfärg på formerna|Insekt|
## **Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över eventuella ändringar som gjorts för allmänheten API, t.ex. tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for .NET. Om du har frågor om någon ändring i listan, vänligen ta upp dem i de[Aspose.Diagram supportforum](https://forum.aspose.com/c/diagram/17).
### **Lägger till Copy-medlem i Shape-klassen**
Copy-medlemmen tar en målforminstans som en parameter för att klona denna form.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Shape newShape = new Shape();

// copy diagram

newShape.Copy(diagram.Pages[0].Shapes[0]);

newShape.ID = 3;

newShape.XForm.PinX.Value = 1;

newShape.XForm.PinY.Value = 1;

{{< /highlight >}}
### **Lägger till ToPdf-medlem i Shape-klassen**
ToPdf-medlemmen konverterar en form till formatet PDF.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// save a shape in the PDF format

diagram.Pages[0].Shapes.GetShape(59).ToPdf("e:\\out.pdf");

{{< /highlight >}}
### **Lägger till ToHTML-medlem i Shape-klassen**
ToHTML-medlemmen konverterar en form till formatet PDF.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Aspose.Diagram.Saving.HTMLSaveOptions hs = new Aspose.Diagram.Saving.HTMLSaveOptions();

// save a shape in the PDF format

diagram.Pages[0].Shapes.GetShape(59).ToHTML("e:\\out.pdf", hs);

{{< /highlight >}}
### **Användningsexempel**
Kontrollera listan med hjälpämnen som lagts till i Aspose.Diagram Wiki-dokument:

1. [Kopiera en Visio Shape till en annan Shape-instans](/diagram/sv/net/add-2c-retrieve-2c-copy-and-read-visio-shape-data-html/#add-retrieve-copyandreadvisioshapedata-copyavisioshapetoanothershapeinstance)
1. [Konvertera Visio Shape till PDF](https://docs.aspose.com/diagram/net/convert-a-visio-shape-to-pdf/)
1. [Konvertera Visio Shape till HTML](https://docs.aspose.com/diagram/net/convert-a-visio-shape-to-html/)
