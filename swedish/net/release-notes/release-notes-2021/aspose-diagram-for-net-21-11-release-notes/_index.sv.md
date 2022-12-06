---
title: Aspose.Diagram for .NET 21.11 Release Notes
type: docs
weight: 2
url: /sv/net/aspose-diagram-for-net-21-11-release-notes/
---
{{% alert color="primary" %}} 

Den här sidan innehåller information om release notes för Aspose.Diagram for .NET 21.11.

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-51111|Gradientfyllning av cirklarna är fel vid konvertering av en VDX till EMF|Förbättring|
|DIAGRAMNET-52377|Lägg till stöd för att ladda vsd med gammal version 3|Förbättring|
|DIAGRAMNET-51364|VSDX till PNG - texten för OLE Embedded-objekt saknas|Insekt|
|DIAGRAMNET-52329|VSDX till HTML - Emojis finns inte i utdata|Insekt|
|DIAGRAMNET-52345|Sidhuvudets sidfot försvinner efter att filen Diagram har sparats|Insekt|
|DIAGRAMNET-52349|Visio till HTML - Vänster och höger kanter är skurna|Insekt|
|DIAGRAMNET-52374|ArgumentOutOfRangeException medan du sparar till PDF|Insekt|
|DIAGRAMNET-52386|Varför kan vissa diagram-sidor dupliceras och vissa inte kan använda Page.Copy()?|Insekt|

## **Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över alla ändringar som gjorts för allmänheten API, såsom tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for .NET. Om du har frågor om någon ändring som anges, vänligen ta upp den på supportforumet Aspose.Diagram.


### **Lägger till förinställt tema i form**
- Tillämpa ett förinställt tema på den här formen.

{{< highlight "java" >}}

shape.PresetTheme = PresetThemeValue.Bubble;

{{< /highlight >}}


### **Lägger till PresetThemeVariant i Shape**
- Använd en förinställd temavariant på den här formen

{{< highlight "java" >}}

shape.PresetThemeVariant = PresetThemeVariantValue.Variant1;

{{< /highlight >}}

### **Lägger till PresetThemeQuickStyle i Shape**
- Tillämpa en förinställd temavariant quickstyle på den här formen

{{< highlight "java" >}}

 shape.PresetThemeQuickStyle = PresetQuickStyleValue.VariantStyle1;

{{< /highlight >}}
