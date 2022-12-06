---
title: Aspose.Diagram for Java 18.3 Release Notes
type: docs
weight: 100
url: /sv/java/aspose-diagram-for-java-18-3-release-notes/
---
{{% alert color="primary" %}} 

 Den här sidan innehåller release notes för[Aspose.Diagram for Java 18.3](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-18-3-release-notes/).

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMJAVA-50592|Lägg till stöd för NewValue-bearbetningsinstruktionerna|Förbättring|
|DIAGRAMJAVA-50150|Kan inte komma åt form TabsCollection-objekt|Insekt|
|DIAGRAMJAVA-50588|Utgång VSDX - en stor form läggs till|Insekt|
|DIAGRAMJAVA-50593|VSDX till SVG - felaktig text och bakgrundsfärger|Insekt|
|DIAGRAMJAVA-50595|Diagram blir svartvitt när du sparar VSDX dokument|Insekt|
### **Lägger till moveTo-medlem i sidklassen**
MoveTo-medlemmen tar målsidans index som en parameter för att flytta sidans position i Visio-ritningen.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page(1);

// move page in the diagram

newPage.moveTo(2);

diagram.save(dataDir + "Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **Användningsexempel**
Kontrollera listan med hjälpämnen som lagts till i Aspose.Diagram Wiki-dokument:

1. [Flytta sidposition i Visio-ritningen]
