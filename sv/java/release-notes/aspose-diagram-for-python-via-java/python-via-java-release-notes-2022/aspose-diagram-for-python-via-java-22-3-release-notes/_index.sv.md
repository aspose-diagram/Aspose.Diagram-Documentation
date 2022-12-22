---
title: Aspose.Diagram för Python via Java 22.3 Release Notes
type: docs
weight: 25
url: /sv/java/aspose-diagram-for-python-via-java-22-3-release-notes/
---
{{% alert color="primary" %}}

Den här sidan innehåller information om release notes för Aspose.Diagram för Python via Java 22.3.

{{% /alert %}}
## **Förbättringar och förändringar**  ##

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMJAVA-50883|Ta reda på saknade teckensnitt och information om teckensnittsersättning från API|Insekt|

## `?`**Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över alla ändringar som gjorts för allmänheten API, såsom tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for Java. Om du har frågor om någon ändring som anges, vänligen ta upp den på supportforumet Aspose.Diagram.

### **Lägger till AddText i sida**
- Lägger till text med definierade PinX och PinY.

{{< highlight "java" >}}
Shape shape = page.addText(1, 1, 2, 2, "Test text", "Calibri", "#a5a5a5", 0.25);
{{< /highlight >}}

