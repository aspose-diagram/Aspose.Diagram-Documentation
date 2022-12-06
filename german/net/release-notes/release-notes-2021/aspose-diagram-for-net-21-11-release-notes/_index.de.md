---
title: Aspose.Diagram for .NET 21.11 Versionshinweise
type: docs
weight: 2
url: /de/net/aspose-diagram-for-net-21-11-release-notes/
---
{{% alert color="primary" %}} 

Diese Seite enthält Versionshinweise für Aspose.Diagram for .NET 21.11.

{{% /alert %}} 
## **Verbesserungen und Änderungen**

|**Taste**|**Zusammenfassung**|**Kategorie**|
|:- |:- |:- |
|DIAGRAMNET-51111|Die Verlaufsfüllung der Kreise ist falsch, wenn ein VDX in EMF konvertiert wird|Erweiterung|
|DIAGRAMNET-52377|Unterstützung für das Laden von vsd mit der alten Version 3 hinzugefügt|Erweiterung|
|DIAGRAMNET-51364|VSDX zu PNG – der Text des eingebetteten OLE-Objekts fehlt|Insekt|
|DIAGRAMNET-52329|VSDX zu HTML - Emojis sind in der Ausgabe nicht vorhanden|Insekt|
|DIAGRAMNET-52345|Kopfzeile und Fußzeile gehen nach dem Speichern der Datei Diagram verloren|Insekt|
|DIAGRAMNET-52349|Visio zu HTML - Linker und rechter Rand werden abgeschnitten|Insekt|
|DIAGRAMNET-52374|ArgumentOutOfRangeException beim Speichern in PDF|Insekt|
|DIAGRAMNET-52386|Warum können einige diagram-Seiten dupliziert werden und einige können Page.Copy() nicht verwenden?|Insekt|

## **Öffentliche API und rückwärtsinkompatible Änderungen**
Im Folgenden finden Sie eine Liste aller Änderungen, die an der öffentlichen API vorgenommen wurden, z. B. hinzugefügte, umbenannte, entfernte oder veraltete Mitglieder, sowie alle nicht abwärtskompatiblen Änderungen, die an Aspose.Diagram for .NET vorgenommen wurden das Aspose.Diagram Support-Forum.


### **Fügt PresetTheme in Shape hinzu**
- Wenden Sie ein voreingestelltes Design auf diese Form an.

{{< highlight "java" >}}

shape.PresetTheme = PresetThemeValue.Bubble;

{{< /highlight >}}


### **Fügt PresetThemeVariant in Form hinzu**
- Wenden Sie eine voreingestellte Designvariante auf diese Form an

{{< highlight "java" >}}

shape.PresetThemeVariant = PresetThemeVariantValue.Variant1;

{{< /highlight >}}

### **Fügt PresetThemeQuickStyle in Form hinzu**
- Wenden Sie eine voreingestellte Themenvariante Quickstyle auf diese Form an

{{< highlight "java" >}}

 shape.PresetThemeQuickStyle = PresetQuickStyleValue.VariantStyle1;

{{< /highlight >}}
