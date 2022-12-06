---
title: Aspose.Diagram for .NET 21.12 Release Notes
type: docs
weight: 1
url: /sv/net/aspose-diagram-for-net-21-12-release-notes/
---
{{% alert color="primary" %}} 

Den här sidan innehåller information om release notes för Aspose.Diagram for .NET 21.12.

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-52408|problem när vi använder EmfRederSetting EmfPlusPrefer|Förbättring|
|DIAGRAMNET-52438|SaveForegroundPagesEndast för utskrift|Förbättring|
|DIAGRAMNET-52450|Visio till SVG - Sparar rasterbild separat|Förbättring|
|DIAGRAMNET-51171|Delvis återgivning av formerna när du sparar ritning i PDF-format|Insekt|
|DIAGRAMNET-51390|Det inbäddade objektet har inte ersatts korrekt|Insekt|
|DIAGRAMNET-51800|Visio till SVG - Bakgrundsbild saknas (PowerPoint läggs till i VISIO)|Insekt|
|DIAGRAMNET-52423|Page.Copy() kopierar inte Excel-objekt i diagram|Insekt|
|DIAGRAMNET-52443|Saknade former när du öppnar och sparar MS Visio Diagram|Insekt|
|DIAGRAMNET-52444|Visio till JPG - Olika resultat genererade av API|Insekt|
|DIAGRAMNET-52445|Konvertering av provet i Linux- och Windows-miljön har olika resultat|Insekt|

## **Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över alla ändringar som gjorts för allmänheten API, såsom tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for .NET. Om du har frågor om någon ändring som anges, vänligen ta upp den på supportforumet Aspose.Diagram.


### **Lägger till IsSavingImageSeparately i SVGSaveOptions**
- Definierar om bilden ska sparas separat.

{{< highlight "java" >}}

    SVGSaveOptions o = new SVGSaveOptions();
    o.IsSavingImageSeparately = true;

{{< /highlight >}}


### **Lägger till CustomImagePath i SVGSaveOptions**
- Användarens anpassade sökväg (URL) sparad i genererad svg-fil för bilden. Om den inte har definierats av användaren kommer den aktuella katalogen att användas.

{{< highlight "java" >}}

  o.CustomImagePath = "d:/output/";

{{< /highlight >}}

### **Lägger till SaveForegroundPagesOnly i PrintSaveOptions**
- Anger om alla sidor ska skrivas ut eller bara förgrunden.

{{< highlight "java" >}}

 PrintSaveOptions options = new PrintSaveOptions();
 options.SaveForegroundPagesOnly = true;

{{< /highlight >}}
