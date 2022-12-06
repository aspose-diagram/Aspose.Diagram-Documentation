---
title: Aspose.Diagram for .NET 20.1 Versionshinweise
type: docs
weight: 70
url: /de/net/aspose-diagram-for-net-20-1-release-notes/
---
{{% alert color="primary" %}} 

Diese Seite enthält Versionshinweise für Aspose.Diagram for .NET 20.1.

{{% /alert %}} 
## **Verbesserungen und Änderungen**

|**Taste**|**Zusammenfassung**|**Kategorie**|
|:- |:- |:- |
|DIAGRAMNET-51198|Der Schatten auf der Hyperlink-Schaltfläche wird beim Speichern von VSDM in SVG nicht korrekt gerendert|Erweiterung|
|DIAGRAMNET-51526|VSDX zu PDF – Verlaufsfüllung für Pfeilspitzen, die im resultierenden PDF verloren gehen|Erweiterung|
|DIAGRAMNET-51539|Der Farbverlauf in Formen ist im Ausgabe-SVG verloren gegangen|Erweiterung|
|DIAGRAMNET-50705|VSD zum SVG-Export - Formen vom Typ Meta verwandeln sich in chaotische Symbole|Insekt|
|DIAGRAMNET-51664|Die Datei wird beschädigt, nachdem das unbenutzte Design entfernt wurde|Insekt|
|DIAGRAMNET-51665|Bilder werden nach dem Entfernen nicht verwendeter Designs als X angezeigt|Insekt|
|DIAGRAMNET-51684|Beim Entfernen unbenutzter Masterformen und -stile hat nur das Bild ein Problem|Insekt|
|DIAGRAMNET-51726|Hintergrundbild fehlt (PowerPoint wird in VISIO hinzugefügt), während unbenutzte Masterformen und -stile entfernt werden|Insekt|
|DIAGRAMNET-51737|Visio zu HTML – Problem mit der Bildgröße|Insekt|
|DIAGRAMNET-51743|Private Informationen aus Visio entfernen – das Problem mit der Dokumentengröße Visio|Insekt|
|DIAGRAMNET-51745|Seltsamer Fehler tritt in der WPF-Anwendung auf, wenn VSD in VSDX konvertiert wird|Insekt|

## **Öffentliche API und rückwärtsinkompatible Änderungen**
- Seiten zu Ladeoptionen hinzugefügt – Gibt den Index der zu ladenden Seiten an.



{{< highlight "java" >}}

Aspose.Diagram.LoadOptions options = new Aspose.Diagram.LoadOptions(LoadFileFormat.VSDX);

options.Pages = new ArrayList();

options.Pages.Add(0);

{{< /highlight >}}

- SetFontSources in FontConfigs hinzugefügt - Legt die Quellen der Schriftarten fest

{{< highlight "java" >}}

Aspose.Diagram.MemoryFontSource sc1 = new Aspose.Diagram.MemoryFontSource(b);

Aspose.Diagram.MemoryFontSource sc2 = new Aspose.Diagram.MemoryFontSource(b);

Aspose.Diagram.MemoryFontSource[]sc = new Aspose.Diagram.MemoryFontSource[]{ sc1, sc2 };

Aspose.Diagram.FontConfigs.SetFontSources(sc); 

{{< /highlight >}}
