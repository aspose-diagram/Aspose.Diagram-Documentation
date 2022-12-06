---
title: Aspose.Diagram for .NET 19.8 Versionshinweise
type: docs
weight: 50
url: /de/net/aspose-diagram-for-net-19-8-release-notes/
---
{{% alert color="primary" %}} 

Diese Seite enthält Versionshinweise für[Aspose.Diagram for .NET 19.8](https://www.nuget.org/packages/Aspose.Diagram/19.8.0)

{{% /alert %}} 
## **Verbesserungen und Änderungen**

|**Taste**|**Zusammenfassung**|**Kategorie**|
|:- |:- |:- |
|DIAGRAMNET-50334|Unterstützung von VBA-Codes / Makros hinzufügen (Hinzufügen - Bearbeiten - Löschen)|Erweiterung|
|DIAGRAMNET-51083|Unterstützung für das Zeichnen von Splines hinzugefügt|Erweiterung|
|DIAGRAMNET-51676|Visio zu HTML - Ausgabe enthält Dateinamen|Erweiterung|
|DIAGRAMNET-50263|Die Position des Konnektortexts kann nicht als Formeln festgelegt werden|Insekt|
|DIAGRAMNET-50284|VTX in HTML-Konvertierung, Formenfüllfarbe wird nicht beibehalten|Insekt|
|DIAGRAMNET-50432|VDX in PDF-Konvertierung, Diagram.setFontDirs-Methode verwendet nur die erste Schriftart über die gesamte diagram|Insekt|
|DIAGRAMNET-50463|VSDX in PDF-Konvertierung, fehlende oder unvollständige Wiedergabe von Formen|Insekt|
|DIAGRAMNET-51033|Die Netzwerkformen bleiben beim Konvertieren von VSDX in PDF nicht erhalten|Insekt|
|DIAGRAMNET-51303|VSDX zu PDF - Textfarbe auf Verbindungslinien wird geändert|Insekt|
|DIAGRAMNET-51663|Beim Konvertieren von VSD in VSDX tritt eine nicht behandelte Ausnahme auf|Insekt|
|DIAGRAMNET-51664|Die Datei wird nach dem Entfernen eines nicht verwendeten Designs beschädigt|Insekt|
|DIAGRAMNET-51665|Bilder werden nach dem Entfernen nicht verwendeter Designs als X angezeigt|Insekt|
|DIAGRAMNET-51667|Beim Entfernen von Stilen hat nur ein Bild ein Problem|Insekt|
|DIAGRAMNET-51668|VISIO zu JPG - Ausgabebild hat nicht das richtige Format|Insekt|
|DIAGRAMNET-51671|Beim Entfernen unbenutzter Masterformen und -stile hat nur das Bild ein Problem|Insekt|
|DIAGRAMNET-51672|Verlorene Bilder beim Laden und Speichern|Insekt|
|DIAGRAMNET-51677|Visio zu HTML - Link in generiertem HTML funktioniert nicht|Insekt|
|DIAGRAMNET-51678|Visio zu HTML - Falsches Datumsformat beim Speichern als HTML|Insekt|
|DIAGRAMNET-51679|Visio zu PDF - Mehrere Formatierungsfehler in PDF|Insekt|
## **Öffentliche API und rückwärts inkompatible Änderungen**
Im Folgenden finden Sie eine Liste aller Änderungen, die an der öffentlichen API vorgenommen wurden, z. B. hinzugefügte, umbenannte, entfernte oder veraltete Mitglieder, sowie alle nicht abwärtskompatiblen Änderungen, die an Aspose.Diagram for .NET vorgenommen wurden. Wenn Sie Bedenken zu einer der aufgeführten Änderungen haben, äußern Sie diese bitte das[Aspose.Diagram Support-Forum](https://forum.aspose.com/c/diagram/17).
### **Fügt DrawSpline in Seite hinzu**
Das folgende Code-Snippet zeigt, wie man einen Spline zeichnet:

{{< highlight "java" >}}

 PointF[]ps = new PointF[]{ new PointF(0, 0.3270758925347308f), 

                             new PointF(0.2926845121364643f, 0.3581517392187368f), 

                             new PointF(0.6526026522346893f, 0.4640748257705201f), 

                             new PointF(1f, 0.327075892534732f) };

                             diagram.Pages[0].DrawSpline(1, 1, 2, 2, ps);

{{< /highlight >}}
### **Fügt SaveTitle in HTMLSaveOptions hinzu**
Das folgende Code-Snippet definiert, ob Sie den Titel speichern möchten oder nicht:

{{< highlight "java" >}}

 Aspose.Diagram.Saving.HTMLSaveOptions options = new Aspose.Diagram.Saving.HTMLSaveOptions();

options.SaveTitle = false;

{{< /highlight >}}




