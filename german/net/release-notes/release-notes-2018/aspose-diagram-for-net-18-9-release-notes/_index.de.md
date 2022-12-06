---
title: Aspose.Diagram for .NET 18.9 Versionshinweise
type: docs
weight: 40
url: /de/net/aspose-diagram-for-net-18-9-release-notes/
---
{{% alert color="primary" %}} 

 Diese Seite enthält Versionshinweise für[Aspose.Diagram for .NET 18.9](https://www.nuget.org/packages/Aspose.Diagram/18.9.0).

{{% /alert %}} 
## **Verbesserungen und Änderungen**

|**Taste**|**Zusammenfassung**|**Kategorie**|
|:- |:- |:- |
|DIAGRAMNET-51509|VSDX zu PNG - Liniendeckkraft geht im Ausgabebild verloren|Erweiterung|
|DIAGRAMNET-51510|VSDX zu SVG - Liniendeckkraft geht im Ausgabebild verloren|Erweiterung|
|DIAGRAMNET-51516|Führen Sie mehrere VISIO-Dateien zu einer einzigen Ausgabe zusammen|Erweiterung|
|DIAGRAMNET-50272|VSD in SVG-Konvertierung - Einige Verbindungspunkte haben falsche Position und Größe|Insekt|
|DIAGRAMNET-50273|VSD zu SVG – Die Ausrichtung von Formtextelementen ist falsch|Insekt|
|DIAGRAMNET-50487|VSD zu HTML - Schrägstrich zwischen den Werten ist falsch platziert|Insekt|
|DIAGRAMNET-50975|VSDX als PDF - Hintergrundfarbe der Form ist schwarz|Insekt|
|DIAGRAMNET-50976|VSDX to HTML - Hintergrundfarbe der Form ist schwarz|Insekt|
|DIAGRAMNET-50980|VSDX bis PNG - Zahlen in den Rautenformen sind falsch platziert|Insekt|
|DIAGRAMNET-51129|Die Textelemente werden beim Konvertieren von VSD in PDF nicht richtig ausgerichtet|Insekt|
|DIAGRAMNET-51511|Zusätzliche Pfeilspitzen bei der PNG-Konvertierung|Insekt|
|DIAGRAMNET-51512|Zusätzliche Pfeilspitzen, die bei der SVG-Konvertierung angezeigt werden|Insekt|
## **Öffentliche API und rückwärts inkompatible Änderungen**
Im Folgenden finden Sie eine Liste aller Änderungen, die an der öffentlichen API vorgenommen wurden, z. B. hinzugefügte, umbenannte, entfernte oder veraltete Mitglieder, sowie alle nicht abwärtskompatiblen Änderungen, die an Aspose.Diagram for .NET vorgenommen wurden. Wenn Sie Bedenken zu einer der aufgeführten Änderungen haben, äußern Sie diese bitte das[Aspose.Diagram Support-Forum](https://forum.aspose.com/c/diagram/17).
#### **Combine-Methode in Klasse Diagram hinzugefügt**
Kombiniert ein Diagram-Objekt mit einem anderen Diagram-Objekt.

{{< highlight "java" >}}

             Diagram diagramF = new Diagram( "f.vsdx");

            Diagram diagramS = new Diagram( "s.vsdx");

            diagramF.Combine(diagramS);

{{< /highlight >}}
