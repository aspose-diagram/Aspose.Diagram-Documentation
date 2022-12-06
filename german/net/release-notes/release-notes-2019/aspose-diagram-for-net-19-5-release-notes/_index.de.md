---
title: Aspose.Diagram for .NET 19.5 Versionshinweise
type: docs
weight: 80
url: /de/net/aspose-diagram-for-net-19-5-release-notes/
---
{{% alert color="primary" %}} 

Diese Seite enthält Versionshinweise für[Aspose.Diagram for .NET 19.5](https://www.nuget.org/packages/Aspose.Diagram/19.5.0)

{{% /alert %}} 
## **Verbesserungen und Änderungen**

|**Taste**|**Zusammenfassung**|**Kategorie**|
|:- |:- |:- |
|DIAGRAMNET-51606|Erkennen und entfernen Sie ungenutzte Designs, Datengrafiken und Stile aus Visio-Diagrammen|Erweiterung|
|DIAGRAMNET-51637|Verschachtelte Form in einem gruppierten Container wird nicht korrekt beibehalten|Erweiterung|
|DIAGRAMNET-51638|Prop.Value.Val kann nicht abgerufen werden, wenn der Wert eine Ganzzahl ist|Erweiterung|
|DIAGRAMNET-51640|Ermitteln Sie nicht verwendete Stile in einer Visio-Datei|Erweiterung|
|DIAGRAMNET-50051|VSDX in PDF-Konvertierung, fehlender Verbindungspfeil zusammen mit falsch platziertem Text|Insekt|
|DIAGRAMNET-50052|VSDX in PDF-Konvertierung, Formen mit falscher Schrifttextfarbe|Insekt|
|DIAGRAMNET-51179|Falsche Schattierung über einer E-Mail-Schaltfläche beim Konvertieren einer VSDM in SVG|Insekt|
|DIAGRAMNET-51190|Falsche Anzeige der Form mit Hyperlink beim Speichern einer VDX in SVG|Insekt|
|DIAGRAMNET-51194|Falsche Darstellung eines Symbols beim Speichern einer VDX in SVG|Insekt|
|DIAGRAMNET-51254|Falsche Schattierung in der oberen Leiste beim Konvertieren einer VSDM in SVG|Insekt|
|DIAGRAMNET-51618|Visio zu PDF - Ungültiges Datumsformat und fehlende Daten|Insekt|
|DIAGRAMNET-51628|Falscher Textwert für gelöschten Standardtext in 0,vsdx-Diagrammen|Insekt|
|DIAGRAMNET-51634|Visio zu SVG - Falscher Z-Index einiger Formen in der Ausgabe|Insekt|
|DIAGRAMNET-51636|Visio zu SVG - nicht alle Pfadelemente werden korrekt als Rect-Elemente exportiert|Insekt|
|DIAGRAMNET-51641|Zusätzliches Bild wird angezeigt, wenn Visio mit API erneut gespeichert wird|Insekt|
## **Öffentliche API und rückwärts inkompatible Änderungen**
Im Folgenden finden Sie eine Liste aller Änderungen, die an der öffentlichen API vorgenommen wurden, z. B. hinzugefügte, umbenannte, entfernte oder veraltete Mitglieder, sowie alle nicht abwärtskompatiblen Änderungen, die an Aspose.Diagram for .NET vorgenommen wurden. Wenn Sie Bedenken zu einer der aufgeführten Änderungen haben, äußern Sie diese bitte das[Aspose.Diagram Support-Forum](https://forum.aspose.com/c/diagram/17).
### **Fügt GetUnusedStyles in Diagram hinzu**
Holen Sie sich ungenutzte Stile.

{{< highlight "java" >}}

  StyleSheetCollection unused = diagram.GetUnusedStyles();

{{< /highlight >}}
