---
title: Aspose.Diagram for .NET 21.3 Versionshinweise
type: docs
weight: 10
url: /de/net/aspose-diagram-for-net-21-3-release-notes/
---
{{% alert color="primary" %}} 

Diese Seite enthält Versionshinweise für Aspose.Diagram for .NET 21.3.

{{% /alert %}} 
## **Verbesserungen und Änderungen**

|**Taste**|**Zusammenfassung**|**Kategorie**|
|:- |:- |:- |
|DIAGRAMNET-51967|Verkleinern und drucken Sie eine Diagram auf einer Seite|Erweiterung|
|DIAGRAMNET-51995|Probleme mit Aspose.Diagram-Dateien und Skyline Dataminer|Erweiterung|
|DIAGRAMNET-51996|CenterDrawing-Methode in Bezug auf die Seite|Erweiterung|
|DIAGRAMNET-52000|IsIntersect funktioniert nicht richtig für diagram|Erweiterung|
|DIAGRAMNET-52003|Kleben Sie die Verbinder mit EndX- und BeginX-Zellen in Form|Erweiterung|
|DIAGRAMNET-51565|VSDX zu PDF - Formen und Hintergrundmuster fehlen|Insekt|
|DIAGRAMNET-51992|Der Export von vsdx nach svg führt zu fehlerhafter Darstellung im IE, Chrome oder Firefox|Insekt|
|DIAGRAMNET-51997|Die Lizenzeinstellung schlägt mit Ausnahme von Aspose.Diagram fehl, wenn die Aspose.Total-Lizenz für alle APIs in der Azure-Funktion verwendet wird|Insekt|
|DIAGRAMNET-51998|Das Geoms-Attribut der Form ist in Version > 20.3.0 eine leere Liste|Insekt|
|DIAGRAMNET-51999|InheritProps kann nicht aktualisiert werden|Insekt|
|DIAGRAMNET-52004|Beim Exportieren von VSDX als SVG fehlen einige Kanten|Insekt|
|DIAGRAMNET-52005|Problem bei der Konvertierung von VSD in VSDX|Insekt|
|DIAGRAMNET-52009|Beim Konvertieren von Visio in HTML fehlen Formen|Insekt|

## ` `**Öffentliche API und rückwärtsinkompatible Änderungen**
` ` Im Folgenden finden Sie eine Liste aller Änderungen, die an der öffentlichen API vorgenommen wurden, z. B. hinzugefügte, umbenannte, entfernte oder veraltete Mitglieder, sowie alle nicht abwärtskompatiblen Änderungen, die an Aspose.Diagram for .NET vorgenommen wurden das Aspose.Diagram Support-Forum.
### **ConnectShapesViaConnector in Seite hinzugefügt**
- Formen über Verbinder verbinden.

{{< highlight "java" >}}

diagram.Pages[pageNumber].ConnectShapesViaConnector(ampShape.ID, "Port7", wssShape.ID, "Port21", lineShape.ID);

{{< /highlight >}}
### **Fügt GlueShapeToConnectorBeginX in Seite hinzu**
- Kleben Sie die Form mit BeginX



{{< highlight "java" >}}

diagram.Pages[pageNumber].GlueShapeToConnectorBeginX(ampShape.ID, "Port7", lineShape.ID);

{{< /highlight >}}
### **Fügt GlueShapeToConnectorEndX in Seite hinzu**
- Kleben Sie die Form mit BeginX



{{< highlight "java" >}}

diagram.Pages[pageNumber].GlueShapeToConnectorEndX(wssShape.ID, "Port21", lineShape.ID);

{{< /highlight >}}
### **Fügt CenterDrawing in Seite hinzu**
- Zentriert die Shapes einer Seite in Bezug auf die Ausdehnung der Seite.



{{< highlight "java" >}}

diagram.Pages[pageNumber].CenterDrawing();

{{< /highlight >}}
### **Fügt IsContain in Shape hinzu**
- Gibt an, ob diese Form eine andere Form enthält.



{{< highlight "java" >}}

OLE_Shape.IsContain(shape)

{{< /highlight >}}



