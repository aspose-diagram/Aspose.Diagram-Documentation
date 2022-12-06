---
title: Aspose.Diagram für Python über Java 21.9 Versionshinweise
type: docs
weight: 6
url: /de/java/aspose-diagram-for-python-via-java-21-9-release-notes/
---
{{% alert color="primary" %}}

Diese Seite enthält Versionshinweise für Aspose.Diagram für Python über Java 21.9.

{{% /alert %}}
## **Verbesserungen und Änderungen**  ##

|**Taste**|**Zusammenfassung**|**Kategorie**|
|:- |:- |:- |
|DIAGRAMJAVA-50753|wk: Überprüfen Sie, ob TextAnnotation mit der Form verbunden ist|Erweiterung|
|DIAGRAMJAVA-50382|Beim Konvertieren einer VSDX in PDF fehlt die Schattierung von Formen|Insekt|
|DIAGRAMJAVA-50754|wk - LineColor von InheritLine ist nicht korrekt|Insekt|
|DIAGRAMJAVA-50756|wk: PinPos null vs Mitte-Mitte|Insekt|
|DIAGRAMJAVA-50757|WK: getBegin/End Arrow-Wert falsch.|Insekt|
|DIAGRAMJAVA-50771|WK: Linienfarbe und Name für Blattform können nicht abgerufen werden|Insekt|
## `?`**Öffentliche API und rückwärtsinkompatible Änderungen**
Im Folgenden finden Sie eine Liste aller Änderungen, die an der öffentlichen API vorgenommen wurden, z. B. hinzugefügte, umbenannte, entfernte oder veraltete Mitglieder, sowie alle nicht abwärtskompatiblen Änderungen, die an Aspose.Diagram for Java vorgenommen wurden das Aspose.Diagram Support-Forum.

### **Fügt „dependsOnShapes“ in Shape hinzu**
- Gibt ein Array zurück, das die Bezeichner der Shapes enthält, die von einem Shape abhängig sind.



{{< highlight "java" >}}

long[]shapeids = shape.dependsOnShapes();

{{< /highlight >}}