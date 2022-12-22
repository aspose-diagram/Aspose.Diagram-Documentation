---
title: Aspose.Diagram for Java 18.2 Release Notes
type: docs
weight: 110
url: /sv/java/aspose-diagram-for-java-18-2-release-notes/
---
{{% alert color="primary" %}} 

 Den här sidan innehåller release notes för[Aspose.Diagram for Java 18.2](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-18-2-release-notes/).

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMJAVA-50587|Lägg till stöd för att hämta relativ Char-element i textdelen|Förbättring|
|DIAGRAMJAVA-50478|Anslutningslinjer passerar genom de andra formerna vid konvertering av en VDX till VSDM|Insekt|
|DIAGRAMJAVA-50581|VSDX till PDF - felaktig återgivning av formerna|Insekt|
|DIAGRAMJAVA-50582|Utgång VSDX - anslutningsledningarna är inte raka|Insekt|
|DIAGRAMJAVA-50583|VSD import - ett fel inträffade i VisioDocument-elementet|Insekt|
|DIAGRAMJAVA-50584|VDX import - ett fel inträffade i VisioDocument-elementet|Insekt|
|DIAGRAMJAVA-50585|VSD import - ett fel inträffade i VisioDocument-elementet|Insekt|
|DIAGRAMJAVA-50586|VSDX till SVG - felaktig kantfärg på formen|Insekt|
### **Lägger till getInheritChars-metoden i Shape-klassen**
Den innehåller char-värdena för formen som ärvs av masterformen.

{{< highlight "java" >}}

 CharCollection charCollection = shape.getInheritChars();

{{< /highlight >}}
