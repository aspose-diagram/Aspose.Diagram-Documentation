---
title: Aspose.Diagram for .NET 22.10 Release Notes
type: docs
weight: 18
url: /sv/net/aspose-diagram-for-net-22-10-release-notes/
---
{{% alert color="primary" %}} 

Den här sidan innehåller information om utgåvor för Aspose.Diagram for .NET 22.10.

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-52988|En bild visas i dålig kvalitet när den exporteras till SVG-format|Förbättring|
|DIAGRAMNET-53002|Förlorad länk vid export till html med Aspose.Diagram|Förbättring|
|DIAGRAMNET-52983|Fel i Diagram.Spara|Insekt|
|DIAGRAMNET-52984|Ändra värden i VentureLicenser-klassen|Insekt|
|DIAGRAMNET-52993|Konversation från vsdx till svg misslyckas|Insekt|
|DIAGRAMNET-52995|App: Laddar vsd ger undantag|Insekt|

## **Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över alla ändringar som gjorts för allmänheten API, såsom tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for .NET. Om du har frågor om någon ändring som anges, vänligen ta upp den på supportforumet Aspose.Diagram.

### **Lägger till GetDisplayText in Shape**
- Få texten som visas i gränssnittet

{{< highlight "java" >}}
String text = shape.GetDisplayText();
{{< /highlight >}}

### **Lägger till InheritGeoms in Shape**
- Innehåller Geoms-värdena för formen som ärvs av huvudformen.

{{< highlight "java" >}}
int count = shape.InheritGeoms.Count;
{{< /highlight >}}