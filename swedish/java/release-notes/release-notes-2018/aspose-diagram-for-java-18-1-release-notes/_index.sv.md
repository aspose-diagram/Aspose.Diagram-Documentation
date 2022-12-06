---
title: Aspose.Diagram for Java 18.1 Release Notes
type: docs
weight: 120
url: /sv/java/aspose-diagram-for-java-18-1-release-notes/
---
{{% alert color="primary" %}} 

 Den här sidan innehåller release notes för[Aspose.Diagram for Java 18.1](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-18-1-release-notes/).

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMJAVA-50200|Lägg till stöd för att duplicera / klona en diagram-sida|Förbättring|
|DIAGRAMJAVA-50408|Ett fel uppstod efter att ha tagit bort en sida från VSDM|Insekt|
|DIAGRAMJAVA-50577|VDX till VSDM - anslutningsledningarna är inte korrekt anslutna|Insekt|
|DIAGRAMJAVA-50578|VDX till VSDM - anslutningsledningarna är inte korrekt anslutna|Insekt|
|DIAGRAMJAVA-50579|Utdata VDX - placera alla Visio former på den samtidiga punkten|Insekt|
|DIAGRAMJAVA-50580|Utdata VDX - felaktig layout av formerna|Insekt|
### **Lägger till Copy-medlem i Sidklass**
Kopieringsmedlemmen tar en målsidesinstans som en parameter för att klona den här sidan.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page(1);

// copy page

newPage.copy(diagram.getPages().get(0));

{{< /highlight >}}
### **Användningsexempel**
Kontrollera listan med hjälpämnen som lagts till i Aspose.Diagram Wiki-dokument:

1. [Kopiera Visio sida till en annan sidinstans]
