---
title: Aspose.Diagram for .NET 19.3 Versionshinweise
type: docs
weight: 100
url: /de/net/aspose-diagram-for-net-19-3-release-notes/
---
{{% alert color="primary" %}} 

Diese Seite enthält Versionshinweise für[Aspose.Diagram for .NET 19.3](https://www.nuget.org/packages/Aspose.Diagram/19.3.0)

{{% /alert %}} 
## **Verbesserungen und Änderungen**

|**Taste**|**Zusammenfassung**|**Kategorie**|
|:- |:- |:- |
|DIAGRAMNET-50930|Unterstützung für das Abrufen gängiger Schriftverzeichnisse auf Betriebssystemen hinzugefügt|Erweiterung|
|DIAGRAMNET-51614|Holen Sie sich alle Props-Werte für eine Form|Erweiterung|
|DIAGRAMNET-50214|VSD in PDF-Konvertierung - Gekrümmte Linien werden zu einer geraden Linie|Insekt|
|DIAGRAMNET-50240|VSD in PDF-Konvertierung - Falsches Layout dynamischer Konnektoren|Insekt|
|DIAGRAMNET-50703|VSDX zu PDF-Export - Fehlender dynamischer Konnektor|Insekt|
|DIAGRAMNET-50704|VSD in PDF-Export - Meta-Typ-Formen werden zu unordentlichen Symbolen|Insekt|
|DIAGRAMNET-51535|VSDM zu SVG – Die Schriftart ändert sich in SVG von Sans zu Serif|Insekt|
|DIAGRAMNET-51574|VSDX zu PNG – Einige Formen werden in der PNG-Ausgabe falsch gerendert|Insekt|
|DIAGRAMNET-51608|Textumbruch funktioniert nicht wie erwartet|Insekt|
|DIAGRAMNET-51609|Formen werden nach links verschoben, wenn Diagram in PowerPoint Slide kopiert wird|Insekt|
|DIAGRAMNET-51617|Visio zu PDF – Externe datengesteuerte Werte werden nicht korrekt angezeigt|Insekt|
|DIAGRAMNET-51619|Visio zu PDF - Falsches Datum/Uhrzeit/Entfernung in PDF|Insekt|
|DIAGRAMNET-51621|Visio zu PDF - Hintergrundbild ist verzerrt und die Extraseite ist im PDF vorhanden|Insekt|
## **Öffentliche API und rückwärts inkompatible Änderungen**
Im Folgenden finden Sie eine Liste aller Änderungen, die an der öffentlichen API vorgenommen wurden, z. B. hinzugefügte, umbenannte, entfernte oder veraltete Mitglieder, sowie alle nicht abwärtskompatiblen Änderungen, die an Aspose.Diagram for .NET vorgenommen wurden. Wenn Sie Bedenken zu einer der aufgeführten Änderungen haben, äußern Sie diese bitte das[Aspose.Diagram Support-Forum](https://forum.aspose.com/c/diagram/17).
### **Fügt GetDefaultFontDir in Diagram hinzu**
Rufen Sie den Ordnerpfad für Standardschriften ab

{{< highlight "java" >}}

  string str =  diagram.GetDefaultFontDir();

{{< /highlight >}}
