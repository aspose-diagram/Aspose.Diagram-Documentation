---
title: Aspose.Diagram for Java 18.2 Versionshinweise
type: docs
weight: 110
url: /de/java/aspose-diagram-for-java-18-2-release-notes/
---
{{% alert color="primary" %}} 

 Diese Seite enthält Versionshinweise für[Aspose.Diagram for Java 18.2](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-18-2-release-notes/).

{{% /alert %}} 
## **Verbesserungen und Änderungen**

|**Taste**|**Zusammenfassung**|**Kategorie**|
|:- |:- |:- |
|DIAGRAMJAVA-50587|Unterstützung für das Abrufen des relativen Char-Elements des Textteils hinzugefügt|Erweiterung|
|DIAGRAMJAVA-50478|Beim Konvertieren von VDX in VSDM verlaufen Verbindungslinien durch die anderen Shapes|Insekt|
|DIAGRAMJAVA-50581|VSDX zu PDF - falsche Darstellung der Formen|Insekt|
|DIAGRAMJAVA-50582|Ausgabe VSDX - die Verbindungslinien sind nicht gerade|Insekt|
|DIAGRAMJAVA-50583|VSD Import – Im VisioDocument-Element ist ein Fehler aufgetreten|Insekt|
|DIAGRAMJAVA-50584|VDX Import – Im VisioDocument-Element ist ein Fehler aufgetreten|Insekt|
|DIAGRAMJAVA-50585|VSD Import – Im VisioDocument-Element ist ein Fehler aufgetreten|Insekt|
|DIAGRAMJAVA-50586|VSDX zu SVG - falsche Rahmenfarbe der Form|Insekt|
### **Fügt die getInheritChars-Methode in der Shape-Klasse hinzu**
Es enthält die Zeichenwerte für das Shape, das vom Master-Shape geerbt wird.

{{< highlight "java" >}}

 CharCollection charCollection = shape.getInheritChars();

{{< /highlight >}}
