---
title: Aspose.Diagram for .NET 18.9 Release Notes
type: docs
weight: 40
url: /sv/net/aspose-diagram-for-net-18-9-release-notes/
---
{{% alert color="primary" %}} 

 Den här sidan innehåller release notes för[Aspose.Diagram for .NET 18.9](https://www.nuget.org/packages/Aspose.Diagram/18.9.0).

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-51509|VSDX till PNG - Linjeopacitet förlorad i utdatabild|Förbättring|
|DIAGRAMNET-51510|VSDX till SVG - Linjeopacitet förlorad i utdatabild|Förbättring|
|DIAGRAMNET-51516|Slå samman flera VISIO-filer till en enda utgång|Förbättring|
|DIAGRAMNET-50272|VSD till SVG-konvertering - Vissa anslutningspunkter har fel position och storlek|Insekt|
|DIAGRAMNET-50273|VSD till SVG - Justeringen av formtextobjekt är felaktig|Insekt|
|DIAGRAMNET-50487|VSD till HTML - snedstreck mellan värdet är felplacerat|Insekt|
|DIAGRAMNET-50975|VSDX till PDF - Bakgrundsfärgen på formen är svart|Insekt|
|DIAGRAMNET-50976|VSDX till HTML - Bakgrundsfärgen på formen är svart|Insekt|
|DIAGRAMNET-50980|VSDX till PNG - Siffrorna inuti diamantformerna är felplacerade|Insekt|
|DIAGRAMNET-51129|Textobjekten är inte korrekt justerade vid konvertering av en VSD till PDF|Insekt|
|DIAGRAMNET-51511|Ytterligare pilspetsar i PNG-konvertering|Insekt|
|DIAGRAMNET-51512|Ytterligare pilspetsar visas i SVG-konvertering|Insekt|
## **Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över eventuella ändringar som gjorts för allmänheten API, t.ex. tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for .NET. Om du har frågor om någon ändring i listan, vänligen ta upp dem i de[Aspose.Diagram supportforum](https://forum.aspose.com/c/diagram/17).
#### **Lade till Kombinera metod i Diagram Klass**
Kombinerar ett Diagram-objekt med ett annat Diagram-objekt.

{{< highlight "java" >}}

             Diagram diagramF = new Diagram( "f.vsdx");

            Diagram diagramS = new Diagram( "s.vsdx");

            diagramF.Combine(diagramS);

{{< /highlight >}}
