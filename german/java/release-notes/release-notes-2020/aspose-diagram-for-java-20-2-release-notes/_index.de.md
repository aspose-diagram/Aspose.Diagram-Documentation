---
title: Aspose.Diagram for Java 20.2 Versionshinweise
type: docs
weight: 60
url: /de/java/aspose-diagram-for-java-20-2-release-notes/
---
{{% alert color="primary" %}} 

Diese Seite enthält Versionshinweise für Aspose.Diagram for Java 20.2.

{{% /alert %}} 
## **Verbesserungen und Änderungen**

|**Taste**|**Zusammenfassung**|**Kategorie**|
|:- |:- |:- |
|DIAGRAMJAVA-50361|The shape foreground color is not being preserved on converting a VST to PNG|Erweiterung|
|DIAGRAMJAVA-50504|VSD to PDF - the color of lines is changed|Erweiterung|
## ` `**Öffentliche API und rückwärtsinkompatible Änderungen**
Im Folgenden finden Sie eine Liste aller Änderungen, die an der öffentlichen API vorgenommen wurden, z. B. hinzugefügte, umbenannte, entfernte oder veraltete Mitglieder, sowie alle nicht abwärtskompatiblen Änderungen, die an Aspose.Diagram for Java vorgenommen wurden das Aspose.Diagram Support-Forum.
### **VergrößernSeite in ImageSaveOptions hinzugefügt**
- Gibt an, ob die Seite vergrößert werden soll

{{< highlight "java" >}}

 com.aspose.diagram.ImageSaveOptions o = new com.aspose.diagram.ImageSaveOptions(SaveFileFormat.PNG);

opt.setEnlargePage(false);

{{< /highlight >}}
### **hasHiddenInfo in Diagram hinzugefügt**
- Gibt an, ob diese diagram versteckte Informationen enthält

{{< highlight "java" >}}

 diagram.hasHiddenInfo();

{{< /highlight >}}




