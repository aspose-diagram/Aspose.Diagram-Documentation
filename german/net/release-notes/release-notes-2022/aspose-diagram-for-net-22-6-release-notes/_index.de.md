---
title: Aspose.Diagram for .NET 22.6 Versionshinweise
type: docs
weight: 22
url: /de/net/aspose-diagram-for-net-22-6-release-notes/
---
{{% alert color="primary" %}} 

Diese Seite enthält Versionshinweise für Aspose.Diagram for .NET 22.6.

{{% /alert %}} 
## **Verbesserungen und Änderungen**

|**Taste**|**Zusammenfassung**|**Kategorie**|
|:- |:- |:- |
|DIAGRAMNET-52826|Defekter Link beim Speichern von VSDM als PDF|Erweiterung|
|DIAGRAMNET-52851|Einige Formen verlieren nach der Umwandlung in SVG ihre Rundung|Erweiterung|
|DIAGRAMNET-52858|Bildqualität in HTML|Erweiterung|
|DIAGRAMNET-52825|Problem beim Export nach HTML|Insekt|
|DIAGRAMNET-52832|Visio zu PDF/SVG - Gedrehte Textposition geändert|Insekt|
|DIAGRAMNET-52840|Elemente in der HTML-Vorschau verschwommen|Insekt|
|DIAGRAMNET-52842|Seite automatisch anpassen wird nicht automatisch angepasst|Insekt|
|DIAGRAMNET-52849|Rasterbilder werden nach der Konvertierung nicht herunterskaliert|Insekt|
|DIAGRAMNET-52852|VSD Fehler beim Öffnen - Aspose.Diagram.DiagramException|Insekt|

## **Öffentliche API und rückwärts inkompatible Änderungen**
Im Folgenden finden Sie eine Liste aller Änderungen, die an der öffentlichen API vorgenommen wurden, z. B. hinzugefügte, umbenannte, entfernte oder veraltete Mitglieder, sowie alle nicht abwärtskompatiblen Änderungen, die an Aspose.Diagram for .NET vorgenommen wurden das Aspose.Diagram Support-Forum.
### **Fügt Auflösung in HTMLSaveOptions hinzu**
- Ruft die Auflösung für das generierte HTML in Punkten pro Zoll ab oder legt sie fest.

{{< highlight "java" >}}
HTMLSaveOptions option = new HTMLSaveOptions();
option.Resolution = 96;
{{< /highlight >}}
