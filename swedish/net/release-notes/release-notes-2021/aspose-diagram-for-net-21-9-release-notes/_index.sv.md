---
title: Aspose.Diagram for .NET 21.9 Release Notes
type: docs
weight: 4
url: /sv/net/aspose-diagram-for-net-21-9-release-notes/
---
{{% alert color="primary" %}} 

Den här sidan innehåller information om release notes för Aspose.Diagram for .NET 21.9.

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-50164|Revidera layouten för CompactTree-alternativet fungerar inte som förväntat|Förbättring|
|DIAGRAMNET-50997|Kan inte ställa in layoutalternativen för en VDX diagram|Förbättring|
|DIAGRAMNET-52117|Lägg till stöd för avbokningstoken på Diagram-metoden|Förbättring|
|DIAGRAMNET-52196|Laddar och sparar vsdx förlorad fälttext|Förbättring|
|DIAGRAMNET-52197|Laddar och sparar vsdx ändra värde för DisplayMode|Förbättring|
|DIAGRAMNET-52205|Dubbelklickshändelse saknas i form|Förbättring|
|DIAGRAMNET-51877|Undantaget "Parametern är inte giltig" när VSD-filen renderas|Insekt|
|DIAGRAMNET-52114|"Parametern är inte giltig." undantag när VSD-filen renderas till PNG/JPG|Insekt|
|DIAGRAMNET-52124|Sparar Visio som html-problem|Insekt|
|DIAGRAMNET-52127|Sparar Visio med hjälplinjer till HTML ärendet|Insekt|
|DIAGRAMNET-52148|VSDX till PDF - Genomstruken text är inte korrekt i PDF|Insekt|
|DIAGRAMNET-52150|Det går inte att extrahera värdet för den användardefinierade cellformeln CONT.|Insekt|
|DIAGRAMNET-52229|Användardefinierad cell byts namn|Insekt|
|DIAGRAMNET-52231|Anslutningen för att forma "lim" alternativet har förlorats|Insekt|
|DIAGRAMNET-52252|Formkontur avskuren när du sparar visio till html|Insekt|
|DIAGRAMNET-52253|Efter att ha sparat .vtx-filen till .vsdx är den tillagda kontakten från stencilen trasig|Insekt|
|DIAGRAMNET-52266|Kan inte ta bort användardefinierade celler|Insekt|

## **Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över alla ändringar som gjorts för allmänheten API, såsom tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for .NET. Om du har frågor om någon ändring som anges, vänligen ta upp den på supportforumet Aspose.Diagram.

### **Lägger till DependsOnShapes i Shape**
- Returnerar en array som innehåller identifierarna för de former som är beroende av en form.



{{< highlight "java" >}}

long[]shapeids = shape.DependsOnShapes();

{{< /highlight >}}



