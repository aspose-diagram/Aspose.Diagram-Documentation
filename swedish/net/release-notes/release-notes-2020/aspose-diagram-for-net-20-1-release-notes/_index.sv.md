---
title: Aspose.Diagram for .NET 20.1 Release Notes
type: docs
weight: 70
url: /sv/net/aspose-diagram-for-net-20-1-release-notes/
---
{{% alert color="primary" %}} 

Den här sidan innehåller information om release notes för Aspose.Diagram for .NET 20.1.

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-51198|Skugga på hyperlänk-knappen renderas inte korrekt när VSDM sparas till SVG|Förbättring|
|DIAGRAMNET-51526|VSDX till PDF - Gradientfyllning för pilspetsar som förloras i resulterande PDF|Förbättring|
|DIAGRAMNET-51539|Gradienten i former har förlorats i utdata SVG|Förbättring|
|DIAGRAMNET-50705|VSD till SVG-export - Metatyper förvandlas till röriga symboler|Insekt|
|DIAGRAMNET-51664|Filen blir skadad efter borttagning av oanvänt tema|Insekt|
|DIAGRAMNET-51665|Bilder visas som X efter att oanvända teman har tagits bort|Insekt|
|DIAGRAMNET-51684|När du tar bort oanvända masterformer och stilar är det bara bilden som har ett problem|Insekt|
|DIAGRAMNET-51726|Bakgrundsbild saknas (PowerPoint läggs till i VISIO) samtidigt som oanvända masterformer och stilar tas bort|Insekt|
|DIAGRAMNET-51737|Visio till Html - bildstorlek Issue|Insekt|
|DIAGRAMNET-51743|Ta bort privat information från Visio - problemet med Visio dokumentstorlek|Insekt|
|DIAGRAMNET-51745|Konstigt fel uppstår i WPF-applikationen vid konvertering av VSD till VSDX|Insekt|

## **Offentlig API och bakåtinkompatibla ändringar**
- Added Pages to LoadOptions - Anger indexet för de sidor som ska laddas.



{{< highlight "java" >}}

Aspose.Diagram.LoadOptions options = new Aspose.Diagram.LoadOptions(LoadFileFormat.VSDX);

options.Pages = new ArrayList();

options.Pages.Add(0);

{{< /highlight >}}

- Lade till SetFontSources i FontConfigs - Ställer in teckensnittskällorna

{{< highlight "java" >}}

Aspose.Diagram.MemoryFontSource sc1 = new Aspose.Diagram.MemoryFontSource(b);

Aspose.Diagram.MemoryFontSource sc2 = new Aspose.Diagram.MemoryFontSource(b);

Aspose.Diagram.MemoryFontSource[]sc = new Aspose.Diagram.MemoryFontSource[]{ sc1, sc2 };

Aspose.Diagram.FontConfigs.SetFontSources(sc); 

{{< /highlight >}}
