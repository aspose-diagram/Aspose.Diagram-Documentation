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
|DIAGRAMJAVA-50551|VSDX zu PNG - falsche Darstellung der Formecken|Insekt|
|DIAGRAMJAVA-50552|Die Füllfarben werden beim Speichern einer Visio-Zeichnung in SVG nicht beibehalten|Insekt|
|DIAGRAMJAVA-50553|Falsches Rendering von Linien beim Speichern einer Visio-Zeichnung in SVG|Insekt|
|DIAGRAMJAVA-50554|Die Füllfarben werden beim Speichern einer Visio-Zeichnung in SVG nicht beibehalten|Insekt|
|DIAGRAMJAVA-50555|Falsches Rendering von Linien beim Speichern einer Visio-Zeichnung in SVG|Insekt|
|DIAGRAMJAVA-50559|VSDM bis VDX - die Verbindungslinien sind nicht mit den Shapes verbunden|Insekt|
|DIAGRAMJAVA-50561|Die Zeichnung VSDX ist nach dem Hinzufügen des SolutionXML-Elements beschädigt|Insekt|
### **Fügt SameAsPdfConversionArea in ImageSaveOptions hinzu**
Es gibt an, ob der Bereich auf die gleiche Weise wie bei PDF gespeichert werden soll.

{{< highlight "java" >}}

 String dataDir = "C:\\temp\\";

// load a drawing

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// specify image save options

ImageSaveOptions opts = new ImageSaveOptions(SaveFileFormat.PNG);

opts.setSameAsPdfConversionArea(true);

{{< /highlight >}}
