---
title: Aspose.Diagram for .NET 18.10 Versionshinweise
type: docs
weight: 30
url: /de/net/aspose-diagram-for-net-18-10-release-notes/
---
{{% alert color="primary" %}} 

 Diese Seite enthält Versionshinweise für[Aspose.Diagram for .NET 18.10](https://www.nuget.org/packages/Aspose.Diagram/18.10.0).

{{% /alert %}} 
## **Verbesserungen und Änderungen**

|**Taste**|**Zusammenfassung**|**Kategorie**|
|:- |:- |:- |
|DIAGRAMNET-51527|Bilder gehen nach der Konvertierung von VSDM in SVG verloren|Erweiterung|
|DIAGRAMNET-51532|VSD zu PDF - Schatten des Bildes ist nicht korrekt|Erweiterung|
|DIAGRAMNET-51536|Der Schatten der Form wurde nach VSDX zur SVG-Konvertierung entfernt|Erweiterung|
|DIAGRAMNET-51544|Die Unterstreichung wird nach der Konvertierung von VSDM in SVG aus dem Text entfernt|Erweiterung|
|DIAGRAMNET-51558|Implementieren Sie Getter für Shape.ConnectorsType|Erweiterung|
|DIAGRAMNET-51520|VDX an HTML - Zusätzliche Zeilen erscheinen in der Ausgabe|Insekt|
|DIAGRAMNET-51521|Die Schriftart in diagram wird geändert, nachdem VSD als VSDX gespeichert wurde|Insekt|
|DIAGRAMNET-51523|VSDX bis SVG - Pfeilspitzen fehlen|Insekt|
|DIAGRAMNET-51524|VSDM zu SVG - Blaue Kreuze wurden in der Ausgabedatei angezeigt|Insekt|
|DIAGRAMNET-51525|Form der Entscheidung ändert sich von Diamant zu Quadrat, während VSDM zu SVG-Konvertierung|Insekt|
|DIAGRAMNET-51528|Form der Entscheidung ändert sich von Diamant zu Quadrat, während VSDM zu SVG-Konvertierung|Insekt|
|DIAGRAMNET-51529|VSDM zu SVG - Gepunktete Linien werden in gefüllte Linien umgewandelt|Insekt|
|DIAGRAMNET-51531|Formen werden nach der Konvertierung von VSDX in SVG auf die rechte Seite verschoben|Insekt|
|DIAGRAMNET-51533|Rote Kreuze erschienen nach der VISIO-zu-SVG-Konvertierung|Insekt|
|DIAGRAMNET-51534|Ein roter Punkt erschien in der unteren linken Ecke der Form|Insekt|
|DIAGRAMNET-51538|Bilder gehen nach der Konvertierung von VSDX in PDF verloren|Insekt|
|DIAGRAMNET-51541|Text ist nach der Konvertierung von VSDX in SVG unsichtbar|Insekt|
|DIAGRAMNET-51542|Text wurde nach VSDX zur SVG-Konvertierung gelöscht|Insekt|
|DIAGRAMNET-51543|Das Zeit- und Datumsformat wird nach VSDM in SVG geändert|Insekt|
|DIAGRAMNET-51545|VSDX zu SVG - Text wird in der Ausgabe umbrochen|Insekt|
|DIAGRAMNET-51546|VSDX zu SVG - Text wird in der Ausgabe umbrochen|Insekt|
|DIAGRAMNET-51547|VSDX zu SVG - Text wird in der Ausgabe umbrochen|Insekt|
|DIAGRAMNET-51548|VSDX zu SVG - Text wird in der Ausgabe umbrochen|Insekt|
|DIAGRAMNET-51551|Korrekte Themenfarbe von Formen kann nicht abgerufen werden|Insekt|
|DIAGRAMNET-51552|Umgekehrte Pfeilspitzen, die bei der SVG-Konvertierung angezeigt werden|Insekt|
|DIAGRAMNET-51559|Problem mit der Textgrößenänderung beim Konvertieren von VSDM in SVG|Insekt|
|DIAGRAMNET-51560|Verbindungslinien werden nach der Konvertierung in SVG dünn|Insekt|
## **Öffentliche API und rückwärts inkompatible Änderungen**
Im Folgenden finden Sie eine Liste aller Änderungen, die an der öffentlichen API vorgenommen wurden, z. B. hinzugefügte, umbenannte, entfernte oder veraltete Mitglieder, sowie alle nicht abwärtskompatiblen Änderungen, die an Aspose.Diagram for .NET vorgenommen wurden. Wenn Sie Bedenken zu einer der aufgeführten Änderungen haben, äußern Sie diese bitte das[Aspose.Diagram Support-Forum](https://forum.aspose.com/c/diagram/17).
#### **InheritLine in Form hinzugefügt**
Enthält die Linienformatierungswerte für die Form, die von der übergeordneten Formatvorlage und der Masterform übernommen werden.

{{< highlight "java" >}}

 		Line line = shape.InheritLine;

{{< /highlight >}}


#### **GetConnectorsType in Shape hinzugefügt**
Konnektortyp abrufen

{{< highlight "java" >}}

 Shapes.GetShape(1).GetConnectorsType()

{{< /highlight >}}

