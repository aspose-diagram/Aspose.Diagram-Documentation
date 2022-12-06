---
title: Aspose.Diagram for .NET 19.5 Release Notes
type: docs
weight: 80
url: /sv/net/aspose-diagram-for-net-19-5-release-notes/
---
{{% alert color="primary" %}} 

Den här sidan innehåller release notes för[Aspose.Diagram for .NET 19.5](https://www.nuget.org/packages/Aspose.Diagram/19.5.0)

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-51606|Upptäck och ta bort oanvända teman, datagrafik och stilar från Visio Diagram|Förbättring|
|DIAGRAMNET-51637|Kapslad form inuti en grupperad behållare bevaras inte korrekt|Förbättring|
|DIAGRAMNET-51638|Det går inte att få Prop.Value.Val när värdet är ett heltal|Förbättring|
|DIAGRAMNET-51640|Bestäm oanvända stilar i en Visio-fil|Förbättring|
|DIAGRAMNET-50051|VSDX till PDF-konvertering, anslutningspil saknas tillsammans med felplacerad text|Insekt|
|DIAGRAMNET-50052|VSDX till PDF-konvertering, former med felaktig teckenfärg|Insekt|
|DIAGRAMNET-51179|Felaktig skuggning över en e-postknapp vid konvertering av en VSDM till SVG|Insekt|
|DIAGRAMNET-51190|Felaktig visning av hyperlänkad form när en VDX sparades till SVG|Insekt|
|DIAGRAMNET-51194|Felaktig återgivning av en ikon när en VDX sparades till SVG|Insekt|
|DIAGRAMNET-51254|Felaktig skuggning i det översta fältet vid konvertering av en VSDM till SVG|Insekt|
|DIAGRAMNET-51618|Visio till PDF - Dåligt datumformat och saknade data|Insekt|
|DIAGRAMNET-51628|Felaktigt textvärde för raderad standardtext i .vsdx-diagram|Insekt|
|DIAGRAMNET-51634|Visio till SVG - Fel z-index för vissa former i utdata|Insekt|
|DIAGRAMNET-51636|Visio till SVG - inte alla sökvägselement är korrekt exporterade som rect-element|Insekt|
|DIAGRAMNET-51641|Extra bild visas när du sparar om Visio med API|Insekt|
## **Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över eventuella ändringar som gjorts för allmänheten API, t.ex. tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for .NET. Om du har frågor om någon ändring i listan, vänligen ta upp dem i de[Aspose.Diagram supportforum](https://forum.aspose.com/c/diagram/17).
### **Lägger till GetUnusedStyles i Diagram**
Skaffa oanvända stilar.

{{< highlight "java" >}}

  StyleSheetCollection unused = diagram.GetUnusedStyles();

{{< /highlight >}}
