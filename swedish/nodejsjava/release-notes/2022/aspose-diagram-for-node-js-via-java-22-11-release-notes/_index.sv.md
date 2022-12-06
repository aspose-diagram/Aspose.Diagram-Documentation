---
title: Aspose.Diagram för Node.js via Java 22.11 Release Notes
type: docs
weight: 17
url: /sv/nodejsjava/aspose-diagram-for-node-js-via-java-22-11-release-notes/
---
{{% alert color="primary" %}}

Den här sidan innehåller information om release notes för Aspose.Diagram för Node.js via Java 22.11.

{{% /alert %}}
## **Förbättringar och förändringar**  ##

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMJAVA-51049|Hur man får anslutningspunkten för en linje på en form|Förbättring|
|DIAGRAMJAVA-51044|.getDisplayText() för att avkoda HTML-entiteter (Aspose.Diagram Java 22.10, .vsd filer)|Förbättring|
|DIAGRAMJAVA-51046|Shapes namn är ibland annorlunda än namnen i Visio|Insekt|

## **Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över alla ändringar som gjorts för allmänheten API, såsom tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for Java. Om du har frågor om någon ändring som anges, vänligen ta upp den på supportforumet Aspose.Diagram.

### **Lägger till getConnectorRule i Shape**
- Returnerar en connectorRule som innehåller form-id och connecton som är anslutna till formen

{{< highlight "java" >}}
ConnectorRule rule= shape.getConnectorRule();
{{< /highlight >}}

### **Lägger till setSavingCustomLinePattern i SVGSaveOptions**
- Definierar om Sparar anpassat linjemönster.

{{< highlight "java" >}}
SVGSaveOptions saveOp = new SVGSaveOptions(); 
saveOp.setSavingCustomLinePattern(false);
{{< /highlight >}}
