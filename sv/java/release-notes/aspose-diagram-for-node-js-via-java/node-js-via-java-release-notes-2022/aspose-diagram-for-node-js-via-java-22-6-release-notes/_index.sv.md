---
title: Aspose.Diagram för Node.js via Java 22.6 Release Notes
type: docs
weight: 22
url: /sv/java/aspose-diagram-for-node-js-via-java-22-6-release-notes/
---
{{% alert color="primary" %}}

Den här sidan innehåller information om release notes för Aspose.Diagram för Node.js via Java 22.6.

{{% /alert %}}
## **Förbättringar och förändringar**  ##

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMJAVA-50963|WK: Formen förvrängd efter att ha sparats till PNG|Förbättring|
|DIAGRAMJAVA-50967|Ändra storlek på sidolinjeformen [Forts.]|Insekt|
|DIAGRAMJAVA-50972|API analyserar inte filen korrekt|Insekt|
|DIAGRAMJAVA-50974|Problem med att lägga till ny anslutningspunkt|Insekt|

## `?`**Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över alla ändringar som gjorts för allmänheten API, såsom tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for Java. Om du har frågor om någon ändring som anges, vänligen ta upp den på supportforumet Aspose.Diagram.

### **Lägger till upplösning i HTMLSaveOptions**
- Hämtar eller ställer in upplösningen för den genererade HTML-koden, i punkter per tum.

{{< highlight "java" >}}
HTMLSaveOptions option = new HTMLSaveOptions();
option.setResolution(96);
{{< /highlight >}}
