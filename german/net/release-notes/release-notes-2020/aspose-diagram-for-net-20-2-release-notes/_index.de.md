---
title: Aspose.Diagram for .NET 20.2 Versionshinweise
type: docs
weight: 60
url: /de/net/aspose-diagram-for-net-20-2-release-notes/
---
{{% alert color="primary" %}} 

Diese Seite enthält Versionshinweise für Aspose.Diagram for .NET 20.2.

{{% /alert %}} 
## **Verbesserungen und Änderungen**

|**Taste**|**Zusammenfassung**|**Kategorie**|
|:- |:- |:- |
|DIAGRAMNET-51747|Dateiänderungen nach Visio vsd->vsdx Konvertierung|Erweiterung|
|DIAGRAMNET-51750|Flag "HasHiddenInfo" hinzufügen|Erweiterung|
|DIAGRAMNET-51748|PNG zu Diagram hinzufügen - Transparenz geht verloren|Insekt|
|DIAGRAMNET-51749|Beim Speichern des Dokuments Visio tritt ein Fehler auf|Insekt|
|DIAGRAMNET-51751|VSDX zu PNG - Zusätzliches Bild wird angezeigt|Insekt|
|DIAGRAMNET-51752|VSDX bis PNG - Zusätzliches Leerzeichen wird angezeigt|Insekt|
|DIAGRAMNET-51753|VSDX zu PNG - Die Position der Symbole ändert sich|Insekt|
|DIAGRAMNET-51754|VSDX zu PNG - Die Position des Fragezeichensymbols wurde geändert|Insekt|
|DIAGRAMNET-51762|Das generierte PDF unterscheidet sich von der Eingabe Visio diagram|Insekt|
|DIAGRAMNET-51763|VSDX bis PNG - In der Ausgabe fehlen Informationen|Insekt|
## ` `**Öffentliche API und rückwärtsinkompatible Änderungen**
` ` Im Folgenden finden Sie eine Liste aller Änderungen, die an der öffentlichen API vorgenommen wurden, z. B. hinzugefügte, umbenannte, entfernte oder veraltete Mitglieder, sowie alle nicht abwärtskompatiblen Änderungen, die an Aspose.Diagram for .NET vorgenommen wurden das Aspose.Diagram Support-Forum.
### **EnlargePage in ImageSaveOptions hinzugefügt**
- Gibt an, ob die Seite vergrößert werden soll

{{< highlight "java" >}}

 Aspose.Diagram.Saving.ImageSaveOptions opt = new Aspose.Diagram.Saving.ImageSaveOptions(Aspose.Diagram.SaveFileFormat.PNG);

opt.EnlargePage = false;

{{< /highlight >}}
### **HasHiddenInfo in Diagram hinzugefügt**
- Gibt an, ob diese diagram versteckte Informationen enthält.



{{< highlight "java" >}}

 diagram.HasHiddenInfo();

{{< /highlight >}}




