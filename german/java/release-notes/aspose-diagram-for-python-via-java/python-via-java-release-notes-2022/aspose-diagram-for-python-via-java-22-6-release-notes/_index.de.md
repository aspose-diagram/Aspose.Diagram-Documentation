---
title: Aspose.Diagram für Python über Java 22.6 Versionshinweise
type: docs
weight: 22
url: /de/java/aspose-diagram-for-python-via-java-22-6-release-notes/
---
{{% alert color="primary" %}}

Diese Seite enthält Versionshinweise für Aspose.Diagram für Python über Java 22.6.

{{% /alert %}}
## **Verbesserungen und Änderungen**  ##

|**Taste**|**Zusammenfassung**|**Kategorie**|
|:- |:- |:- |
|DIAGRAMJAVA-50963|WK: Form nach dem Speichern in PNG verzerrt|Erweiterung|
|DIAGRAMJAVA-50967|Größe der Seitenlinienform ändern [Forts.]|Insekt|
|DIAGRAMJAVA-50972|API analysiert die Datei nicht richtig|Insekt|
|DIAGRAMJAVA-50974|Problem beim Hinzufügen eines neuen Verbindungspunkts|Insekt|

## `?`**Öffentliche API und rückwärtsinkompatible Änderungen**
Im Folgenden finden Sie eine Liste aller Änderungen, die an der öffentlichen API vorgenommen wurden, z. B. hinzugefügte, umbenannte, entfernte oder veraltete Mitglieder, sowie alle nicht abwärtskompatiblen Änderungen, die an Aspose.Diagram for Java vorgenommen wurden das Aspose.Diagram Support-Forum.

### **Fügt Auflösung in HTMLSaveOptions hinzu**
- Ruft die Auflösung für das generierte HTML in Punkten pro Zoll ab oder legt sie fest

{{< highlight "java" >}}
HTMLSaveOptions option = new HTMLSaveOptions();
option.setResolution(96);
{{< /highlight >}}
