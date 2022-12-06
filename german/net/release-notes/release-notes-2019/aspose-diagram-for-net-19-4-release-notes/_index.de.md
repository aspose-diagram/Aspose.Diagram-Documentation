---
title: Aspose.Diagram for .NET 19.4 Versionshinweise
type: docs
weight: 90
url: /de/net/aspose-diagram-for-net-19-4-release-notes/
---
{{% alert color="primary" %}} 

Diese Seite enthält Versionshinweise für[Aspose.Diagram for .NET 19.4](https://www.nuget.org/packages/Aspose.Diagram/19.4.0)

{{% /alert %}} 
## **Verbesserungen und Änderungen**

|**Taste**|**Zusammenfassung**|**Kategorie**|
|:- |:- |:- |
|DIAGRAMNET-51602|Eingebettetes XSLX-Objekt wird nach Manipulation beschädigt|Erweiterung|
|DIAGRAMNET-51625|Externe Excel-Daten in .vsdx-Dateien werden beim erneuten Speichern von Diagram entfernt|Erweiterung|
|DIAGRAMNET-51626|API verarbeitet keine Excel-Daten|Erweiterung|
|DIAGRAMNET-51627|Extrahieren Sie Formdaten auf der Grundlage der Dependson-Formel|Erweiterung|
|DIAGRAMNET-51629|Das Vergrößern einer Seite, um sie an eine Zeichnung anzupassen, scheint nicht zu funktionieren|Erweiterung|
|DIAGRAMNET-51176|Die Verlaufstitelleiste wird beim Konvertieren von VSDM in SVG geändert|Insekt|
|DIAGRAMNET-51404|VSD bis Bild - Die Formfarbe ist dunkel|Insekt|
|DIAGRAMNET-51473|VDX zu PDF - Die falsche Hintergrundfarbe|Insekt|
|DIAGRAMNET-51475|VSDX in PDF - Die Farbverläufe werden umgekehrt gerendert|Insekt|
|DIAGRAMNET-51616|Visio zu PDF – Farbverlauf wird im Ausgabe-PDF auf dem Kopf stehend dargestellt|Insekt|
|DIAGRAMNET-51630|VSDX an HTML – Die Hintergrundfarbe von Formen ist in der Ausgabe nicht vorhanden|Insekt|
|DIAGRAMNET-51631|VSDX zu PDF - Hintergrundfarbe von Formen ist in der Ausgabe nicht vorhanden|Insekt|
|DIAGRAMNET-51632|VSD in SVG – Objekt vom Typ „ “ kann nicht in Typ „ “ umgewandelt werden. Ausnahme aufgetreten|Insekt|

## **Öffentliche API und rückwärts inkompatible Änderungen**
Im Folgenden finden Sie eine Liste aller Änderungen, die an der öffentlichen API vorgenommen wurden, z. B. hinzugefügte, umbenannte, entfernte oder veraltete Mitglieder, sowie alle nicht abwärtskompatiblen Änderungen, die an Aspose.Diagram for .NET vorgenommen wurden. Wenn Sie Bedenken zu einer der aufgeführten Änderungen haben, äußern Sie diese bitte das[Aspose.Diagram Support-Forum](https://forum.aspose.com/c/diagram/17).
### **Fügt Aufzählung RemoveHiddenInfoItem hinzu**
Gibt das Entfernen versteckter Informationen für diagram an.
### **Fügt RemoveHiddenInfoItem in Diagram hinzu**
Entfernen Sie ungenutzte Informationen.

{{< highlight "java" >}}

diagram.RemoveHiddenInformation((int)(RemoveHiddenInfoItem.Shapes | RemoveHiddenInfoItem.Masters));

{{< /highlight >}}
