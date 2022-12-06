---
title: Aspose.Diagram for .NET 22.1 Versionshinweise
type: docs
weight: 27
url: /de/net/aspose-diagram-for-net-22-1-release-notes/
---
{{% alert color="primary" %}} 

Diese Seite enthält Versionshinweise für Aspose.Diagram for .NET 22.1.

{{% /alert %}} 
## **Verbesserungen und Änderungen**

|**Taste**|**Zusammenfassung**|**Kategorie**|
|:- |:- |:- |
|DIAGRAMNET-50560|Unterstützt das Speichern von Diagrammen in HTML mit oder ohne eingebettete Ressourcen|Erweiterung|
|DIAGRAMNET-52499|Unterstützung für das Speichern von HTML in einem einzelnen Stream hinzufügen|Erweiterung|
|DIAGRAMNET-50562|VSDX zu PDF - Formen fehlen in der Ausgabe|Insekt|
|DIAGRAMNET-50780|Beim Speichern einer VSDX als PDF sind die Umrandungslinien der Tabellen nicht sichtbar|Insekt|
|DIAGRAMNET-50962|Beim Konvertieren einer VSDX in PNG fehlen die Umrandungslinien von Tabellen|Insekt|
|DIAGRAMNET-50992|Beim Konvertieren einer VSDX nach PDF ist die linke Begrenzungslinie der Tabelle nicht sichtbar|Insekt|
|DIAGRAMNET-51034|Beim Konvertieren einer VSDX in PDF fehlt die Schattierung von Formen|Insekt|
|DIAGRAMNET-51186|Falsches Layout von Metatypformen beim Konvertieren von VSD in PDF|Insekt|
|DIAGRAMNET-51226|Aspose.Diagram 17.3.0: Beim Speichern im HTML-Stream werden keine externen Ressourcen eingebettet|Insekt|
|DIAGRAMNET-52506|Page.Copy() kopiert die Änderungen des Entwicklers nicht|Insekt|

## **Öffentliche API und rückwärtsinkompatible Änderungen**
Im Folgenden finden Sie eine Liste aller Änderungen, die an der öffentlichen API vorgenommen wurden, z. B. hinzugefügte, umbenannte, entfernte oder veraltete Mitglieder, sowie alle nicht abwärtskompatiblen Änderungen, die an Aspose.Diagram for .NET vorgenommen wurden das Aspose.Diagram Support-Forum.


### **Fügt SaveAsSingleFile in HTMLSaveOptions hinzu**
- Gibt an, ob die HTML-Datei als einzelne Datei gespeichert werden soll.

{{< highlight "java" >}}

    HTMLSaveOptions ho = new HTMLSaveOptions();
    ho.SaveAsSingleFile = true;

{{< /highlight >}}