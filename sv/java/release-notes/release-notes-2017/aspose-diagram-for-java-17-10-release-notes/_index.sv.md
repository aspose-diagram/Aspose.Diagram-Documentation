---
title: Aspose.Diagram for Java 17.10 Release Notes
type: docs
weight: 30
url: /sv/java/aspose-diagram-for-java-17-10-release-notes/
---
{{% alert color="primary" %}} 

 Den här sidan innehåller release notes för[Aspose.Diagram for Java 17.10](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-17-10-release-notes/).

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMJAVA-50560|JpegQuality har ingen effekt på utdatadokument|Förbättring|
|DIAGRAMJAVA-50548|Utgång VSDX - förbindelselinjen som går genom formens gräns|Insekt|
|DIAGRAMJAVA-50550|Sektionen Shape Transform bevarar inte formler|Insekt|
|DIAGRAMJAVA-50551|VSDX till PNG - felaktig återgivning av formhörnen|Insekt|
|DIAGRAMJAVA-50552|Fyllningsfärgerna bevaras inte när en Visio-ritning sparas till SVG|Insekt|
|DIAGRAMJAVA-50553|Felaktig rendering av linjer när du sparar en Visio-ritning till SVG|Insekt|
|DIAGRAMJAVA-50554|Fyllningsfärgerna bevaras inte när en Visio-ritning sparas till SVG|Insekt|
|DIAGRAMJAVA-50555|Felaktig rendering av linjer när du sparar en Visio-ritning till SVG|Insekt|
|DIAGRAMJAVA-50559|VSDM till VDX - förbindningslinjerna är inte kopplade till formerna|Insekt|
|DIAGRAMJAVA-50561|VSDX-ritningen är korrupt efter att ha lagt till SolutionXML-element|Insekt|
### **Lägger till SameAsPdfConversionArea i ImageSaveOptions**
Den anger om området ska sparas på samma sätt som PDF.

{{< highlight "java" >}}

 String dataDir = "C:\\temp\\";

// load a drawing

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// specify image save options

ImageSaveOptions opts = new ImageSaveOptions(SaveFileFormat.PNG);

opts.setSameAsPdfConversionArea(true);

{{< /highlight >}}
