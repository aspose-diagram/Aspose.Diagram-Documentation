---
title: Aspose.Diagram for .NET 22.5 Release Notes
type: docs
weight: 23
url: /sv/net/aspose-diagram-for-net-22-5-release-notes/
---
{{% alert color="primary" %}} 

Den här sidan innehåller information om release notes för Aspose.Diagram for .NET 22.5.

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-52802|Formel/värde uppdaterar inte fält|Förbättring|
|DIAGRAMNET-52803|VSDX till HTML: Utdatafil sparas inte i Async-metoden förrän programmet körs helt|Förbättring|
|DIAGRAMNET-52793|API fungerar inte med en giltig licensversion 22.4|Insekt|
|DIAGRAMNET-52806|Förskjuten indrag i PDF från VSDX|Insekt|
|DIAGRAMNET-52807|Text som finns i tabellen tas bort när .vsdx-filen konverteras till pdf [CONT.]|Insekt|
|DIAGRAMNET-52808|Problem med att konvertera VSDX till PDF [CONT.]|Insekt|
|DIAGRAMNET-52810|Visio former som sparats som bilder är fel|Insekt|
|DIAGRAMNET-52811|Former saknas efter att du har sparat Visio till HTML|Insekt|

## **Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över alla ändringar som gjorts för allmänheten API, såsom tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for .NET. Om du har frågor om någon ändring som anges, vänligen ta upp den på supportforumet Aspose.Diagram.
### **Lägger till DisplayValue in Field**
- Hämtar det formaterade strängvärdet för detta fält.

{{< highlight "java" >}}
String str = shape.Fields[0].DisplayValue;
{{< /highlight >}}

### **Lägger till InheritParas i Shape**
- Innehåller paragraferna för formen som ärvs av moderstilen och mastern

{{< highlight "java" >}}
ParaCollection paras = shape.InheritParas;
Console.WriteLine(paras[0].HorzAlign.Value);
{{< /highlight >}}