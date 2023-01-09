---
title: Aspose.Diagram for Java 17.10 Versionshinweise
type: docs
weight: 30
url: /de/java/aspose-diagram-for-java-17-10-release-notes/
---
{{% alert color="primary" %}} 

 Diese Seite enthält Versionshinweise für[Aspose.Diagram for Java 17.10](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-17-10-release-notes/).

{{% /alert %}} 
## **Verbesserungen und Änderungen**

|**Taste**|**Zusammenfassung**|**Kategorie**|
|:- |:- |:- |
|DIAGRAMJAVA-50560|JPEGQuality wirkt sich nicht auf das Ausgabedokument aus|Erweiterung|
|DIAGRAMJAVA-50548|Ausgabe VSDX - die Verbindungslinie, die durch die Grenze der Form verläuft|Insekt|
|DIAGRAMJAVA-50550|Der Abschnitt Formtransformation behält keine Formeln bei|Insekt|
|DIAGRAMJAVA-50551|VSDX to PNG - incorrect rendering of the shape corners|Insekt|
|DIAGRAMJAVA-50552|The fill colors are not being preserved on saving a Visio drawing to SVG|Insekt|
|DIAGRAMJAVA-50553|Incorrect rendering of lines when saving a Visio drawing to SVG|Insekt|
|DIAGRAMJAVA-50554|The fill colors are not being preserved on saving a Visio drawing to SVG|Insekt|
|DIAGRAMJAVA-50555|Incorrect rendering of lines when saving a Visio drawing to SVG|Insekt|
|DIAGRAMJAVA-50559|VSDM bis VDX - die Verbindungslinien sind nicht mit den Shapes verbunden|Insekt|
|DIAGRAMJAVA-50561|Die Zeichnung VSDX ist nach dem Hinzufügen des SolutionXML-Elements beschädigt|Insekt|
### **Fügt SameAsPdfConversionArea in ImageSaveOptions hinzu**
It specifies whether to save area in the same way as PDF.

{{< highlight "java" >}}

 String dataDir = "C:\\temp\\";

// load a drawing

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// specify image save options

ImageSaveOptions opts = new ImageSaveOptions(SaveFileFormat.PNG);

opts.setSameAsPdfConversionArea(true);

{{< /highlight >}}
