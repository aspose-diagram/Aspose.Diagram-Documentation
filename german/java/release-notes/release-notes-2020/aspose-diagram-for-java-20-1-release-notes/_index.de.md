---
title: Aspose.Diagram for Java 20.1 Versionshinweise
type: docs
weight: 70
url: /de/java/aspose-diagram-for-java-20-1-release-notes/
---
{{% alert color="primary" %}} 

Diese Seite enthält Versionshinweise für Aspose.Diagram for Java 20.1.

{{% /alert %}} 
## **Verbesserungen und Änderungen**

|**Taste**|**Zusammenfassung**|**Kategorie**|
|:- |:- |:- |
|DIAGRAMJAVA-50664|Verlaufsfüllung wird beim Export nach SVG nicht unterstützt|Erweiterung|
|DIAGRAMJAVA-50670|Laden von Schriftarten aus dem Speicher zulassen|Erweiterung|
|DIAGRAMJAVA-50681|API dauert lange, um diagram-Datei mit großer Größe zu laden|Erweiterung|
|DIAGRAMJAVA-50381|Die Netzwerkformen bleiben beim Konvertieren von VSDX in PDF nicht erhalten|Insekt|
|DIAGRAMJAVA-50386|Die Bilder werden beim Konvertieren von VSD in SVG mit Farbunterschieden auf den Kopf gestellt|Insekt|
|DIAGRAMJAVA-50679|VSDX zu PDF - Konnektoren fehlen in der Ausgabe|Insekt|
|DIAGRAMJAVA-50680|Visio zu PNG - Ausgabebilder wurden abgeschnitten|Insekt|
## **Öffentliche API und rückwärtsinkompatible Änderungen**
Das Folgende ist eine Liste aller Änderungen, die an der öffentlichen API vorgenommen wurden, z. B. hinzugefügte, umbenannte, entfernte oder veraltete Mitglieder, sowie alle nicht abwärtskompatiblen Änderungen, die an Aspose.Diagram für JAVA vorgenommen wurden. Wenn Sie Bedenken zu einer der aufgeführten Änderungen haben, äußern Sie diese bitte im Aspose.Diagram-Supportforum.

- getPages und setPages in Page hinzugefügt - Gibt den Index der zu ladenden Seiten an.

{{< highlight "java" >}}

 LoadOptions options = new LoadOptions(LoadFileFormat.VSDX);

options.setPages(new ArrayList());

options.getPages().add(0);

{{< /highlight >}}

- Fügt setFontSources in FontConfigs hinzu - Legt die Schriftartquellen fest.

{{< highlight "java" >}}

 byte[]b = new byte[]{ 0 };

com.aspose.diagram.MemoryFontSource sc1 = new com.aspose.diagram.MemoryFontSource(b);

com.aspose.diagram.MemoryFontSource sc2 = new com.aspose.diagram.MemoryFontSource(b);

com.aspose.diagram.MemoryFontSource[]sc = new com.aspose.diagram.MemoryFontSource[]{ sc1, sc2 };

com.aspose.diagram.FontConfigs.setFontSources(sc); 

{{< /highlight >}}


