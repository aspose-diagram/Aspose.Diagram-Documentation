---
title: Aspose.Diagram for .NET 20.5 Versionshinweise
type: docs
weight: 30
url: /de/net/aspose-diagram-for-net-20-5-release-notes/
---
{{% alert color="primary" %}} 

Diese Seite enthält Versionshinweise für Aspose.Diagram for .NET 20.5.

{{% /alert %}} 
## **Verbesserungen und Änderungen**
VSD in PDF-Konvertierung, die richtige Textausrichtung der Formen bleibt nicht erhalten

|**Taste**|**Zusammenfassung**|**Kategorie**|
|:- |:- |:- |
|DIAGRAMNET-51088|Ruft eine falsche Seitenzahl von VSD ab|Erweiterung|
|DIAGRAMNET-51731|Bestimmen Sie, ob eine Form eine andere Form in diagram schneidet|Erweiterung|
|DIAGRAMNET-51833|Aspose.Diagram 20.4: Visio Dokumentversion wird nicht unterstützt|Erweiterung|
|DIAGRAMNET-50361|VSD in PDF-Konvertierung, die richtige Textausrichtung der Formen bleibt nicht erhalten|Insekt|
|DIAGRAMNET-50955|Die Textelemente von Rautenformen werden beim Konvertieren von VSDX in PNG verschoben|Insekt|
|DIAGRAMNET-50990|Außerdem werden Negativ- und Dollarzeichen beim Konvertieren von VSDX in PNG nicht richtig ausgerichtet|Insekt|
|DIAGRAMNET-51815|Eine große Anzahl von Textzeilen in Form kann zu einer offensichtlichen Verschiebung auf der Unterseite führen|Insekt|
|DIAGRAMNET-51820|Bewertungswasserzeichen passt nicht auf eine Seite|Insekt|
|DIAGRAMNET-51821|Visio zu HTML – Probleme mit Bildern und Links in der Ausgabe|Insekt|
|DIAGRAMNET-51823|Konvertieren Sie dabei Visio in SVG. Einige Bilder haben das Problem Icon Missing|Insekt|
|DIAGRAMNET-51824|Konvertieren Sie dabei Visio in SVG. Inhaltsausrichtung falsch|Insekt|
|DIAGRAMNET-51826|Konvertieren Sie dabei Visio in SVG. Symbol fehlt|Insekt|
|DIAGRAMNET-51827|Beim Konvertieren von Visio in SVG - QR-Code fehlt|Insekt|
|DIAGRAMNET-51828|Beim Konvertieren von Visio in SVG - PDF-Symbol fehlt|Insekt|
|DIAGRAMNET-51829|Beim Konvertieren von Visio in SVG - Symbol verloren (fehlt)|Insekt|
|DIAGRAMNET-51830|Beim Konvertieren von Visio in SVG - Bild verloren (fehlt)|Insekt|
|DIAGRAMNET-51831|Visio zu HTML – Probleme mit Bildern und Links in der Ausgabe|Insekt|
|DIAGRAMNET-51834|Visio HTML speichern - falsche Konnektoren|Insekt|

## **Öffentliche API und rückwärts inkompatible Änderungen**
Im Folgenden finden Sie eine Liste aller Änderungen, die an der öffentlichen API vorgenommen wurden, z. B. hinzugefügte, umbenannte, entfernte oder veraltete Mitglieder, sowie alle nicht abwärtskompatiblen Änderungen, die an Aspose.Diagram for .NET vorgenommen wurden das Aspose.Diagram Support-Forum.
### **Fügt IsIntersect in Form hinzu**
- Gibt an, ob diese Form eine andere Form schneidet.

{{< highlight "java" >}}

Shape s1 = diagram.Pages[0].Shapes.GetShape(1);

Shape s2 = diagram.Pages[0].Shapes.GetShape(2);

bool isIntersect = s1.IsIntersect(s2);

{{< /highlight >}}



