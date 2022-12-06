---
title: Aspose.Diagram for .NET 18.1 Release Notes
type: docs
weight: 120
url: /sv/net/aspose-diagram-for-net-18-1-release-notes/
---
{{% alert color="primary" %}} 

 Den här sidan innehåller release notes för[Aspose.Diagram for .NET 18.1](https://www.nuget.org/packages/Aspose.Diagram/18.1.0).

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-50494|Lägg till stöd för att duplicera / klona en diagram-sida|Förbättring|
|DIAGRAMNET-51057|Kommandoknappen saknas efter att ha tagit bort en sida från VSDM|Förbättring|
|DIAGRAMNET-51422|VSDX till PDF - skuggorna ignoreras på processformer|Förbättring|
|DIAGRAMNET-50467|VSD till PDF-konvertering, företagets logotyp är felplacerad|Insekt|
|DIAGRAMNET-50469|VSD till PDF-konvertering, radioformtexten är något högre än vanligt|Insekt|
|DIAGRAMNET-51199|Rubriktexten är inte justerad när du sparar en VSDM till SVG|Insekt|
|DIAGRAMNET-51388|Problem med att ladda och spara vsdx-filer|Insekt|
|DIAGRAMNET-51398|VSD till PNG - textpositionen är felaktig|Insekt|
|DIAGRAMNET-51407|VSD till JPEG - textobjekten är felplacerade|Insekt|
|DIAGRAMNET-51419|Former har inte ändrats korrekt i filen vsdx|Insekt|
|DIAGRAMNET-51420|VSDX-filen blir skadad efter att ha laddats och sparats|Insekt|
|DIAGRAMNET-51421|VSDX till PDF - felaktig teckenfärg på texten|Insekt|
## **Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över eventuella ändringar som gjorts för allmänheten API, t.ex. tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for .NET. Om du har frågor om någon ändring i listan, vänligen ta upp dem i de[Aspose.Diagram supportforum](https://forum.aspose.com/c/diagram/17).
### **Lägger till Copy-medlem i Sidklass**
Copy-medlemmen tar en målsidesinstans som en parameter för att klona den här sidan.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page(1);

// copy diagram

newPage.Copy(diagram.Pages[0]);

{{< /highlight >}}
### **Användningsexempel**
Kontrollera listan med hjälpämnen som lagts till i Aspose.Diagram Wiki-dokument:

1. [Kopiera Visio sida till en annan sidinstans](https://docs.aspose.com/diagram/net/retrieve-get-copy-and-insert-a-page/#copy-visio-page-to-another-page-instance)
