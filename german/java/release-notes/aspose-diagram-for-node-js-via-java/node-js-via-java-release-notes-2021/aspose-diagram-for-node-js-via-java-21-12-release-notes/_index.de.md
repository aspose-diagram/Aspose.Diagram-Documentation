---
title: Aspose.Diagram für Node.js über Java 21.12 Versionshinweise
type: docs
weight: 3
url: /de/java/aspose-diagram-for-node-js-via-java-21-12-release-notes/
---
{{% alert color="primary" %}}

Diese Seite enthält Versionshinweise für Aspose.Diagram für Node.js über Java 21.12.


{{% /alert %}}
## **Verbesserungen und Änderungen**  ##

|**Taste**|**Zusammenfassung**|**Kategorie**|
|:- |:- |:- |
|DIAGRAMJAVA-50838|Text auf geradem Verbindungsstück zentrieren|Insekt|
|DIAGRAMJAVA-50839|Sie müssen einen geraden Verbinder zwischen den Formen zeichnen|Insekt|
## `?`**Öffentliche API und rückwärtsinkompatible Änderungen**
Im Folgenden finden Sie eine Liste aller Änderungen, die an der öffentlichen API vorgenommen wurden, z. B. hinzugefügte, umbenannte, entfernte oder veraltete Mitglieder, sowie alle nicht abwärtskompatiblen Änderungen, die an Aspose.Diagram for Java vorgenommen wurden das Aspose.Diagram Support-Forum.


### **Fügt IsSavingImageSeparately in SVGSaveOptions hinzu**
- Legt fest, ob das Bild separat gespeichert wird.

{{< highlight "java" >}}

    SVGSaveOptions o = new SVGSaveOptions();
    o.setIsSavingImageSeparately(true);

{{< /highlight >}}


### **Fügt CustomImagePath in SVGSaveOptions hinzu**
- Der benutzerdefinierte Pfad (URL) des Benutzers, der in der generierten SVG-Datei für das Bild gespeichert ist. Wenn nicht vom Benutzer definiert, wird das aktuelle Verzeichnis verwendet.

{{< highlight "java" >}}

  o.setCustomImagePath("d:/output/");

{{< /highlight >}}

### **Fügt SaveForegroundPagesOnly in PrintSaveOptions hinzu**
- Gibt an, ob alle Seiten gedruckt werden oder nur der Vordergrund.

{{< highlight "java" >}}

 options.setSaveForegroundPagesOnly(true);

{{< /highlight >}}
