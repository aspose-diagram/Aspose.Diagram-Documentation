---
title: Aspose.Diagram for .NET 22.6 Release Notes
type: docs
weight: 22
url: /sv/net/aspose-diagram-for-net-22-6-release-notes/
---
{{% alert color="primary" %}} 

Den här sidan innehåller information om utgåvor för Aspose.Diagram for .NET 22.6.

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-52826|Trasig länk när du sparar VSDM till PDF|Förbättring|
|DIAGRAMNET-52851|Vissa former tappar sin kurva efter konvertering till svg|Förbättring|
|DIAGRAMNET-52858|Bildkvalitet i HTML|Förbättring|
|DIAGRAMNET-52825|Export till HTML problem|Insekt|
|DIAGRAMNET-52832|Visio till PDF/SVG - Roterad textposition ändrad|Insekt|
|DIAGRAMNET-52840|Element i HTML förhandsgranskning suddiga|Insekt|
|DIAGRAMNET-52842|Autopassningssidan passar inte automatiskt|Insekt|
|DIAGRAMNET-52849|Rasterbilder är inte nedskalade efter konvertering|Insekt|
|DIAGRAMNET-52852|VSD Öppna fel - Aspose.Diagram.DiagramException|Insekt|

## **Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över alla ändringar som gjorts för allmänheten API, såsom tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for .NET. Om du har frågor om någon ändring som anges, vänligen ta upp den på supportforumet Aspose.Diagram.
### **Lägger till upplösning i HTMLSaveOptions**
- Hämtar eller ställer in upplösningen för den genererade HTML-koden, i punkter per tum.

{{< highlight "java" >}}
HTMLSaveOptions option = new HTMLSaveOptions();
option.Resolution = 96;
{{< /highlight >}}
