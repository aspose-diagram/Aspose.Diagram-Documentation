---
title: Aspose.Diagram for .NET 22.4 Release Notes
type: docs
weight: 24
url: /sv/net/aspose-diagram-for-net-22-4-release-notes/
---
{{% alert color="primary" %}} 

Den här sidan innehåller information om utgåvor för Aspose.Diagram for .NET 22.4.

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-52015|Fortsättningsbiljett för #DIAGRAMNET-51995 - Problem med Aspose.Diagram-filer och Skyline Datamine|Förbättring|
|DIAGRAMNET-52707|Ändringar av Shapesheets formel/värde utlöser inte ändringar i beroende celler|Förbättring|
|DIAGRAMNET-50345|VSDX till PDF konvertering, felaktig bakgrundsfärg på formerna|Insekt|
|DIAGRAMNET-50954|Formateringsproblem vid rendering av en tabell och alternativknapp vid konvertering av en VSDX till PNG|Insekt|
|DIAGRAMNET-52708|Textposition konverterar till svg|Insekt|
|DIAGRAMNET-52739|Kulturkänsliga poängformat|Insekt|
|DIAGRAMNET-52759|Text som finns i tabellen tas bort när .vsdx-filen konverteras till pdf|Insekt|
|DIAGRAMNET-52762|VSDX till PDF - Bilden har inte konverterats|Insekt|
|DIAGRAMNET-52779|Ellipser skalas inte när Visio konverteras till SVG|Insekt|

## **Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över alla ändringar som gjorts för allmänheten API, såsom tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for .NET. Om du har frågor om någon ändring som anges, vänligen ta upp den på supportforumet Aspose.Diagram.
### **Lägger till GetPureText in Shape**
- Få textsträngen för en form.

{{< highlight "java" >}}
String text = shape.GetPureText();
{{< /highlight >}}

