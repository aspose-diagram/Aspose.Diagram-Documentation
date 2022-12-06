---
title: Aspose.Diagram for .NET 22.3 Release Notes
type: docs
weight: 25
url: /sv/net/aspose-diagram-for-net-22-3-release-notes/
---
{{% alert color="primary" %}} 

Den här sidan innehåller information om release notes för Aspose.Diagram for .NET 22.3.

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-52667|shape.RefreshShape() fungerar inte för att återspegla ändrat BeginY-värde|Förbättring|
|DIAGRAMNET-52668|Geometri NoShow-formelresultat inte uppdaterade|Förbättring|
|DIAGRAMNET-52655|App: laddar vsd av gammal version och sparar till pdf kastar undantag|Insekt|
|DIAGRAMNET-52661|Inget exempel på att lägga till vattenstämpel till visio ges i dokumentationen|Insekt|
|DIAGRAMNET-52663|Upptäck anpassade linjestilar för form med null master|Insekt|
|DIAGRAMNET-52666|Visio till PDF-konvertering - Problem med datagrafik [Forts.]|Insekt|
|DIAGRAMNET-52684|Undantag vid export till HTML|Insekt|
|DIAGRAMNET-52685|Undantag vid export till HTML|Insekt|
|DIAGRAMNET-52692|Diagram.Spara till MemoryStream med PDF Format kastar ett system.NullReferenceException|Insekt|

## **Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över alla ändringar som gjorts för allmänheten API, såsom tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for .NET. Om du har frågor om någon ändring som anges, vänligen ta upp den på supportforumet Aspose.Diagram.

### **Lägger till AddText i sida**
- Lägger till text med definierade PinX och PinY.

{{< highlight "java" >}}
double pinx = page.PageSheet.PageProps.PageWidth.Value / 2;
double piny = page.PageSheet.PageProps.PageHeight.Value / 2;
double width = page.PageSheet.PageProps.PageWidth.Value;
double height = page.PageSheet.PageProps.PageHeight.Value;
Shape shape = page.AddText(pinx, piny, width, height, "Test text", "Calibri", "#a5a5a5", 0.25);
{{< /highlight >}}
