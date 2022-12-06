---
title: Aspose.Diagram for Java 21.3 Versionshinweise
type: docs
weight: 10
url: /de/java/aspose-diagram-for-java-21-3-release-notes/
---
{{% alert color="primary" %}}

Diese Seite enthält Versionshinweise für Aspose.Diagram for Java 21.3.

{{% /alert %}}
## **Verbesserungen und Änderungen**  ##

|**Taste**|**Zusammenfassung**|**Kategorie**|
|:- |:- |:- |
|DIAGRAMJAVA-50711|NullPointerException löst aus, wenn versucht wird, das Dokument VDX als PNG zu speichern|Erweiterung|
|DIAGRAMJAVA-50713|Problem mit überlappendem Text beim Konvertieren von VSDX in PDF|Erweiterung|
## **Öffentliche API und rückwärts inkompatible Änderungen**
Im Folgenden finden Sie eine Liste aller Änderungen, die an der öffentlichen API vorgenommen wurden, z. B. hinzugefügte, umbenannte, entfernte oder veraltete Mitglieder, sowie alle nicht abwärtskompatiblen Änderungen, die an Aspose.Diagram for Java vorgenommen wurden das Aspose.Diagram Support-Forum.
### **ConnectShapesViaConnector in Seite hinzugefügt**
- Formen über Verbinder verbinden.

{{< highlight "java" >}}

page.connectShapesViaConnector(id, "Port7", id, "Port21", id);

{{< /highlight >}}
### **Fügt GlueShapeToConnectorBeginX in Seite hinzu**
- Kleben Sie die Form mit BeginX



{{< highlight "java" >}}

page.glueShapeToConnectorBeginX(id, "Port7", id);

{{< /highlight >}}
### **Fügt GlueShapeToConnectorEndX in Seite hinzu**
- Kleben Sie die Form mit BeginX



{{< highlight "java" >}}

page.glueShapeToConnectorEndX(id, "Port21", id);

{{< /highlight >}}
### **Fügt CenterDrawing in Seite hinzu**
- Zentriert die Shapes einer Seite in Bezug auf die Ausdehnung der Seite.



{{< highlight "java" >}}

page.centerDrawing();

{{< /highlight >}}
### **Fügt IsContain in Shape hinzu**
- Gibt an, ob diese Form eine andere Form enthält.



{{< highlight "java" >}}

OLE_Shape.isContain(shape)

{{< /highlight >}}