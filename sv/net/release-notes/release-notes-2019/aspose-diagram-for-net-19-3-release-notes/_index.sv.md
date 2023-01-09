---
title: Aspose.Diagram for .NET 19.3 Release Notes
type: docs
weight: 100
url: /sv/net/aspose-diagram-for-net-19-3-release-notes/
---
{{% alert color="primary" %}} 

Den här sidan innehåller release notes för[Aspose.Diagram for .NET 19.3](https://www.nuget.org/packages/Aspose.Diagram/19.3.0)

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-50930|Lägg till stöd för att hämta vanliga teckensnittskataloger på operativsystem|Förbättring|
|DIAGRAMNET-51614|Få alla rekvisitavärden för en form|Förbättring|
|DIAGRAMNET-50214|VSD till PDF konvertering - Böjda linjer blir en rak linje|Insekt|
|DIAGRAMNET-50240|VSD till PDF konvertering - Fel layout av dynamiska kontakter|Insekt|
|DIAGRAMNET-50703|VSDX till PDF export - saknar en dynamisk anslutning|Insekt|
|DIAGRAMNET-50704|VSD till PDF export - Metatyper förvandlas till röriga symboler|Insekt|
|DIAGRAMNET-51535|VSDM till SVG - Teckensnittsändringar från Sans till Serif i SVG|Insekt|
|DIAGRAMNET-51574|VSDX till PNG - Vissa former har gjorts felaktiga i utdata PNG|Insekt|
|DIAGRAMNET-51608|Textomslutning fungerar inte som förväntat|Insekt|
|DIAGRAMNET-51609|Former flyttas till vänster sida när Diagram kopieras till PowerPoint Slide|Insekt|
|DIAGRAMNET-51617|Visio till PDF - Externa datadrivna värden visas inte korrekt|Insekt|
|DIAGRAMNET-51619|Visio till PDF - Felaktigt datum/tid/avstånd i PDF|Insekt|
|DIAGRAMNET-51621|Visio till PDF - Bakgrundsbilden är förvrängd och extrasidan finns i PDF|Insekt|
## **Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över eventuella ändringar som gjorts för allmänheten API, t.ex. tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for .NET. Om du har frågor om någon ändring i listan, vänligen ta upp dem i de[Aspose.Diagram supportforum](https://forum.aspose.com/c/diagram/17).
### **Lägger till GetDefaultFontDir i Diagram**
Hämta sökvägen till mappen för standardteckensnitt

{{< highlight "java" >}}

  string str =  diagram.GetDefaultFontDir();

{{< /highlight >}}
