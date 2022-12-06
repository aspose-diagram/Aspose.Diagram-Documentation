---
title: Aspose.Diagram for .NET 22.1 Release Notes
type: docs
weight: 27
url: /sv/net/aspose-diagram-for-net-22-1-release-notes/
---
{{% alert color="primary" %}} 

Den här sidan innehåller information om release notes för Aspose.Diagram for .NET 22.1.

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-50560|Stöd för att spara diagram till HTML med eller utan inbäddade resurser|Förbättring|
|DIAGRAMNET-52499|Lägg till stöd för att spara html till en enda ström|Förbättring|
|DIAGRAMNET-50562|VSDX till PDF - Former saknas i utgången|Insekt|
|DIAGRAMNET-50780|Kantlinjerna i tabellerna är inte synliga när du sparar en VSDX till PDF|Insekt|
|DIAGRAMNET-50962|Bordslinjerna för tabeller saknas vid konvertering av en VSDX till PNG|Insekt|
|DIAGRAMNET-50992|Tabellens vänstra kantlinje är inte synlig vid konvertering av en VSDX till PDF|Insekt|
|DIAGRAMNET-51034|Skuggningen av former saknas vid konvertering av en VSDX till PDF|Insekt|
|DIAGRAMNET-51186|Felaktig layout av metatypformer vid konvertering av en VSD till PDF|Insekt|
|DIAGRAMNET-51226|Aspose.Diagram 17.3.0: Spara till HTML-ström, bädda inte in externa resurser|Insekt|
|DIAGRAMNET-52506|Page.Copy() kopierar inte utvecklarens ändringar|Insekt|

## **Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över alla ändringar som gjorts för allmänheten API, såsom tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for .NET. Om du har frågor om någon ändring som anges, vänligen ta upp den på supportforumet Aspose.Diagram.


### **Lägger till SaveAsSingleFile i HTMLSaveOptions**
- Anger om HTML-filen sparas som en enda fil.

{{< highlight "java" >}}

    HTMLSaveOptions ho = new HTMLSaveOptions();
    ho.SaveAsSingleFile = true;

{{< /highlight >}}