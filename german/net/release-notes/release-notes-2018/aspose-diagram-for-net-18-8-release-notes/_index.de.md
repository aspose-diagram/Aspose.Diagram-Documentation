---
title: Aspose.Diagram for .NET 18.8 Versionshinweise
type: docs
weight: 50
url: /de/net/aspose-diagram-for-net-18-8-release-notes/
---
{{% alert color="primary" %}} 

 Diese Seite enthält Versionshinweise für[Aspose.Diagram for .NET 18.8](https://www.nuget.org/packages/Aspose.Diagram/18.8.0).

{{% /alert %}} 
## **Verbesserungen und Änderungen**

|**Taste**|**Zusammenfassung**|**Kategorie**|
|:- |:- |:- |
|DIAGRAMNET-51500|Problem beim Rendering zum Bild|Erweiterung|
|DIAGRAMNET-51504|Fügen Sie Unterstützung hinzu, um einen neuen Prüfer zu erstellen|Erweiterung|
|DIAGRAMNET-50953|Die Textelemente werden beim Konvertieren einer VSDX in PNG verschoben|Insekt|
|DIAGRAMNET-51122|Die falsche Position von Textelementen beim Konvertieren einer VSD in PDF|Insekt|
|DIAGRAMNET-51123|Der Text der Formen wird beim Konvertieren einer VSD in PDF verschoben|Insekt|
|DIAGRAMNET-51408|VSD bis Bild - die Zeichen überlappen sich mit Linie|Insekt|
|DIAGRAMNET-51499|Diagram.Save-Methode löst OutOfMemoryException aus|Insekt|
|DIAGRAMNET-51501|Formen überlappen sich in der Datei VDX|Insekt|
|DIAGRAMNET-51505|Punkte fehlen im generierten PDF|Insekt|
## **Öffentliche API und rückwärts inkompatible Änderungen**
Im Folgenden finden Sie eine Liste aller Änderungen, die an der öffentlichen API vorgenommen wurden, z. B. hinzugefügte, umbenannte, entfernte oder veraltete Mitglieder, sowie alle nicht abwärtskompatiblen Änderungen, die an Aspose.Diagram for .NET vorgenommen wurden. Wenn Sie Bedenken zu einer der aufgeführten Änderungen haben, äußern Sie diese bitte das[Aspose.Diagram Support-Forum](https://forum.aspose.com/c/diagram/17).
#### **Prüfer hinzugefügt**
{{< highlight "java" >}}

             Reviewer viewer = new Reviewer();

            viewer.Name.Value = "test";

            viewer.ReviewerID.Value = 3;

{{< /highlight >}}




