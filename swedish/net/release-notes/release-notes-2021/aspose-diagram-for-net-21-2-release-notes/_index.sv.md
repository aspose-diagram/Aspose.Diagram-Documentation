---
title: Aspose.Diagram for .NET 21.2 Release Notes
type: docs
weight: 11
url: /sv/net/aspose-diagram-for-net-21-2-release-notes/
---
{{% alert color="primary" %}} 

Den här sidan innehåller information om release notes för Aspose.Diagram for .NET 21.2.

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-51986|Lägg till centerDrawing-metod som finns på interop visio sida|Förbättring|
|DIAGRAMNET-51987|Implementera en metod för att få ActivePage|Förbättring|
|DIAGRAMNET-51978|Konvertera VSD till VSDX - det går inte att öppna utgången i MS Visio|Insekt|
|DIAGRAMNET-51980|"Ett allmänt fel inträffade i GDI+." undantag vid rendering till HTML VSDX fil|Insekt|
|DIAGRAMNET-51981|Konvertera VSDX till PDF - Former är svarta i utdata-pdf|Insekt|
|DIAGRAMNET-51985|VSDX till VSDX/VDX konvertering: Formfärger ändras till övertoning efter att ha sparats|Insekt|
|DIAGRAMNET-51989|Visio till HTML - Konstig kant i utgången|Insekt|

## ` `**Offentlig API och bakåtinkompatibla ändringar**
` `Följande är en lista över alla ändringar som gjorts för allmänheten API såsom tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for .NET. Om du har frågor om någon ändring i listan, vänligen ta upp det på supportforumet Aspose.Diagram.
### **Lade till ActivePage i Diagram**
- Anger den aktiva sidan

{{< highlight "java" >}}

Page page = diagram.ActivePage;

{{< /highlight >}}
### **Lägger till CenterDrawing in Shape**
- Centrera formen i förhållande till sidans omfattning



{{< highlight "java" >}}

shape.CenterDrawing()

{{< /highlight >}}
### **Lägger till DrawLine i sidan**
- Processen att rita en enda linje.



{{< highlight "java" >}}

 diagram.Pages[0].DrawLine(0,0,1,1);

{{< /highlight >}}



