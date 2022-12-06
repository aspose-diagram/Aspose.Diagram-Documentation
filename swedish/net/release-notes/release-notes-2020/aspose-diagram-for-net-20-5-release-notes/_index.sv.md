---
title: Aspose.Diagram for .NET 20.5 Release Notes
type: docs
weight: 30
url: /sv/net/aspose-diagram-for-net-20-5-release-notes/
---
{{% alert color="primary" %}} 

Den här sidan innehåller information om release notes för Aspose.Diagram for .NET 20.5.

{{% /alert %}} 
## **Förbättringar och förändringar**
VSD till PDF-konvertering, rätt textjustering av formerna bevaras inte

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-51088|Hämtar felaktigt sidantal för en VSD|Förbättring|
|DIAGRAMNET-51731|Bestäm om en form skär en annan form i diagram|Förbättring|
|DIAGRAMNET-51833|Aspose.Diagram 20.4: Visio Dokumentversion stöds inte|Förbättring|
|DIAGRAMNET-50361|VSD till PDF-konvertering, rätt textjustering av formerna bevaras inte|Insekt|
|DIAGRAMNET-50955|Textobjekten i diamantformer förskjuts vid konvertering av en VSDX till PNG|Insekt|
|DIAGRAMNET-50990|Plus, negativa tecken och dollartecken är inte korrekt anpassade vid konvertering av en VSDX till PNG|Insekt|
|DIAGRAMNET-51815|Stor mängd textrader i form kan uppenbarligen skapa förskjutning i undersidan|Insekt|
|DIAGRAMNET-51820|Utvärderingsvattenstämpel passar inte in på en sida|Insekt|
|DIAGRAMNET-51821|Visio till Html - bild- och länkproblem i utdata|Insekt|
|DIAGRAMNET-51823|Medan konvertera Visio till SVG. Vissa bilder har problemikon saknas|Insekt|
|DIAGRAMNET-51824|Medan konvertera Visio till SVG. Innehållsjustering fel|Insekt|
|DIAGRAMNET-51826|Medan konvertera Visio till SVG. Ikon saknas|Insekt|
|DIAGRAMNET-51827|Medan konvertera Visio till SVG - QR-kod saknas|Insekt|
|DIAGRAMNET-51828|Medan konvertera Visio till SVG - PDF-ikon saknas|Insekt|
|DIAGRAMNET-51829|Medan konvertera Visio till SVG - Ikon förlorad (saknas)|Insekt|
|DIAGRAMNET-51830|Medan konvertera Visio till SVG - Bild förlorad (saknas)|Insekt|
|DIAGRAMNET-51831|Visio till HTML - bild- och länkproblem i utdata|Insekt|
|DIAGRAMNET-51834|Visio spara HTML - fel kopplingar|Insekt|

## **Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över alla ändringar som gjorts för allmänheten API, såsom tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for .NET. Om du har frågor om någon ändring som anges, vänligen ta upp den på supportforumet Aspose.Diagram.
### **Lägger till IsIntersect in Shape**
- Indikerar om denna form skär en annan form.

{{< highlight "java" >}}

Shape s1 = diagram.Pages[0].Shapes.GetShape(1);

Shape s2 = diagram.Pages[0].Shapes.GetShape(2);

bool isIntersect = s1.IsIntersect(s2);

{{< /highlight >}}



