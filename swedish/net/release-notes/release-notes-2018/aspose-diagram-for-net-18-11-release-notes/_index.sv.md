---
title: Aspose.Diagram for .NET 18.11 Release Notes
type: docs
weight: 20
url: /sv/net/aspose-diagram-for-net-18-11-release-notes/
---
{{% alert color="primary" %}} 

Den här sidan innehåller release notes för[Aspose.Diagram for .NET 18.11](https://www.nuget.org/packages/Aspose.Diagram/18.11.0)

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-50410|MilestoneHelper - Lägg till stöd för anpassad datumsträngsformatsättare|Förbättring|
|DIAGRAMNET-51568|Lägg till ett alternativ för att ställa in ViewBox i SaveOptions för SVG|Förbättring|
|DIAGRAMNET-51580|Aspose.Diagram skapar SVG med riktlinjer och MS Visio gör det inte|Förbättring|
|DIAGRAMNET-51556|Shape.ToImage-metoden genererar inte korrekta bilder|Insekt|
|DIAGRAMNET-51557|Shape.ToImage-metoden returnerar tomma bilder vid kopia av sidan|Insekt|
|DIAGRAMNET-51570|Shape.ToImage-metoden genererar inte korrekta bilder|Insekt|
|DIAGRAMNET-51576|VSDX till PDF - Textblock saknas|Insekt|
|DIAGRAMNET-51578|VSDX till bildresultat i StackOverFlowException|Insekt|
## **Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över eventuella ändringar som gjorts för allmänheten API, t.ex. tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for .NET. Om du har frågor om någon ändring i listan, vänligen ta upp dem i de[Aspose.Diagram supportforum](https://forum.aspose.com/c/diagram/17).
### **Lägger till SVGFitToViewPort i SVGSaveOptions**
Om den här egenskapen är sann kommer den genererade SVG:en att passa för att visa porten.

{{< highlight "java" >}}

 SVGSaveOptions option = new SVGSaveOptions();

option.SVGFitToViewPort = true;

SVGSaveOptions option = new SVGSaveOptions();

option.SVGFitToViewPort = true;

{{< /highlight >}}
### **Lägger till ExportGuideShapes i RenderingSaveOptions**
Definierar om du behöver exportera guideformerna eller inte.

{{< highlight "java" >}}

 Aspose.Diagram.Saving.SVGSaveOptions o = new SVGSaveOptions();

o.ExportGuideShapes = false;

{{< /highlight >}}
### **Lägger till DateFormatString i MilestoneHelper**
DateFormat sträng av form

{{< highlight "java" >}}

 milestoneHelper.DateFormatString = "yyyy/mm/dd";

{{< /highlight >}}
