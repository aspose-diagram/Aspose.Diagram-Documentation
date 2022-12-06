---
title: Aspose.Diagram for .NET 22.5 Versionshinweise
type: docs
weight: 23
url: /de/net/aspose-diagram-for-net-22-5-release-notes/
---
{{% alert color="primary" %}} 

Diese Seite enthält Versionshinweise für Aspose.Diagram for .NET 22.5.

{{% /alert %}} 
## **Verbesserungen und Änderungen**

|**Taste**|**Zusammenfassung**|**Kategorie**|
|:- |:- |:- |
|DIAGRAMNET-52802|Formel/Wert aktualisiert Felder nicht|Erweiterung|
|DIAGRAMNET-52803|VSDX zu HTML: Die Ausgabedatei wird nicht in der Async-Methode gespeichert, bis das Programm vollständig ausgeführt wurde|Erweiterung|
|DIAGRAMNET-52793|API funktioniert nicht mit einer gültigen Lizenzversion 22.4|Insekt|
|DIAGRAMNET-52806|Versetzter Einzug im PDF von VSDX|Insekt|
|DIAGRAMNET-52807|In der Tabelle vorhandener Text wird beim Konvertieren der .vsdx-Datei in eine PDF-Datei entfernt [FORTS.]|Insekt|
|DIAGRAMNET-52808|Problem beim Konvertieren von VSDX in PDF [FORTS.]|Insekt|
|DIAGRAMNET-52810|Visio Als Bilder gespeicherte Formen sind falsch|Insekt|
|DIAGRAMNET-52811|Formen fehlen nach dem Speichern von Visio in HTML|Insekt|

## **Öffentliche API und rückwärts inkompatible Änderungen**
Im Folgenden finden Sie eine Liste aller Änderungen, die an der öffentlichen API vorgenommen wurden, z. B. hinzugefügte, umbenannte, entfernte oder veraltete Mitglieder, sowie alle nicht abwärtskompatiblen Änderungen, die an Aspose.Diagram for .NET vorgenommen wurden das Aspose.Diagram Support-Forum.
### **Fügt DisplayValue in Feld hinzu**
- Ruft den formatierten Zeichenfolgenwert dieses Felds ab.

{{< highlight "java" >}}
String str = shape.Fields[0].DisplayValue;
{{< /highlight >}}

### **Fügt InheritParas in Form hinzu**
- Enthält die Paras für die Form, die vom übergeordneten Stil und vom Master geerbt wird

{{< highlight "java" >}}
ParaCollection paras = shape.InheritParas;
Console.WriteLine(paras[0].HorzAlign.Value);
{{< /highlight >}}