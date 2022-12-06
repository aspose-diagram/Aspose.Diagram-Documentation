---
title: Aspose.Diagram for .NET 21.3 Release Notes
type: docs
weight: 10
url: /sv/net/aspose-diagram-for-net-21-3-release-notes/
---
{{% alert color="primary" %}} 

Den här sidan innehåller information om release notes för Aspose.Diagram for .NET 21.3.

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-51967|Krympa och skriv ut ett Diagram på en sida|Förbättring|
|DIAGRAMNET-51995|Problem med Aspose.Diagram-filer och Skyline Dataminer|Förbättring|
|DIAGRAMNET-51996|CenterDrawing-metod med avseende på sida|Förbättring|
|DIAGRAMNET-52000|IsIntersect fungerar inte korrekt för en diagram|Förbättring|
|DIAGRAMNET-52003|Limma fast kontakterna med EndX- och BeginX-celler|Förbättring|
|DIAGRAMNET-51565|VSDX till PDF - Former och bakgrundsmönster saknas|Insekt|
|DIAGRAMNET-51992|Exporten från vsdx till svg ger felaktig visning i IE, Chrome eller Firefox|Insekt|
|DIAGRAMNET-51997|Licensinställningen misslyckas med undantag för Aspose.Diagram när Aspose.Total-licensen används för alla API:er i Azure Function|Insekt|
|DIAGRAMNET-51998|formens geoms-attribut är en tom lista i version > 20.3.0|Insekt|
|DIAGRAMNET-51999|Det gick inte att uppdatera inheritProps|Insekt|
|DIAGRAMNET-52004|Exporterar VSDX som SVG vissa kanter saknas|Insekt|
|DIAGRAMNET-52005|Konvertering VSD till VSDX problem|Insekt|
|DIAGRAMNET-52009|Former saknas vid konvertering av Visio till HTML|Insekt|

## ` `**Offentlig API och bakåtinkompatibla ändringar**
` `Följande är en lista över alla ändringar som gjorts för allmänheten API såsom tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for .NET. Om du har frågor om någon ändring i listan, vänligen ta upp det på supportforumet Aspose.Diagram.
### **Lade till ConnectShapesViaConnector på sidan**
- Anslut former via kontakt.

{{< highlight "java" >}}

diagram.Pages[pageNumber].ConnectShapesViaConnector(ampShape.ID, "Port7", wssShape.ID, "Port21", lineShape.ID);

{{< /highlight >}}
### **Lägger till GlueShapeToConnectorBeginX på sidan**
- Limma Shape med BeginX



{{< highlight "java" >}}

diagram.Pages[pageNumber].GlueShapeToConnectorBeginX(ampShape.ID, "Port7", lineShape.ID);

{{< /highlight >}}
### **Lägger till GlueShapeToConnectorEndX i sidan**
- Limma Shape med BeginX



{{< highlight "java" >}}

diagram.Pages[pageNumber].GlueShapeToConnectorEndX(wssShape.ID, "Port21", lineShape.ID);

{{< /highlight >}}
### **Lägger till CenterDrawing på sidan**
- Centrerar en sidas former med hänsyn till sidans omfattning.



{{< highlight "java" >}}

diagram.Pages[pageNumber].CenterDrawing();

{{< /highlight >}}
### **Lägger till IsContain i Shape**
- Anger om denna form innehåller en annan form.



{{< highlight "java" >}}

OLE_Shape.IsContain(shape)

{{< /highlight >}}



