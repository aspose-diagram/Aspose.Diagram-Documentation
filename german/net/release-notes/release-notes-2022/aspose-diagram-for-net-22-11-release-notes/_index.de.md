﻿---
title: Aspose.Diagram for .NET 22.11 Versionshinweise
type: docs
weight: 17
url: /de/net/aspose-diagram-for-net-22-11-release-notes/
---
{{% alert color="primary" %}} 

Diese Seite enthält Versionshinweise für Aspose.Diagram for .NET 22.11.

{{% /alert %}} 
## **Verbesserungen und Änderungen**

|**Taste**|**Zusammenfassung**|**Kategorie**|
|:- |:- |:- |
|DIAGRAMNET-53011|Unterstützung für das Speichern von xaml als Stream hinzugefügt|Erweiterung|
|DIAGRAMNET-53012|Formel aktualisiert Feld nicht|Erweiterung|
|DIAGRAMNET-53024|Formel aktualisiert Feld nicht|Erweiterung|
|DIAGRAMNET-53009|Gespräch von vsdx zu svg verlorenes Bild|Erweiterung|
|DIAGRAMNET-53010|App: Speichern von vsdx in Pdf verlorene Formen|Insekt|
|DIAGRAMNET-53013|Visio to SVG - Custom line patterns|Insekt|
|DIAGRAMNET-53017|Linked area in HTML of VSD has changed to version 22.10.0.0|Insekt|
|DIAGRAMNET-53018|Fehler mit Paras.SpLine|Insekt|
|DIAGRAMNET-53019|Unten links wird eine zusätzliche Linie gezeichnet|Insekt|
|DIAGRAMNET-53033|Werte von Zellen nicht richtig berechnet|Insekt|
|DIAGRAMNET-53034|Formänderung PinX bewirkt eine Höhenänderung|Insekt|

## **Öffentliche API und rückwärts inkompatible Änderungen**
Im Folgenden finden Sie eine Liste aller Änderungen, die an der öffentlichen API vorgenommen wurden, z. B. hinzugefügte, umbenannte, entfernte oder veraltete Mitglieder, sowie alle nicht abwärtskompatiblen Änderungen, die an Aspose.Diagram for .NET vorgenommen wurden das Aspose.Diagram Support-Forum.

### **Fügt GetConnectorRule in Shape hinzu**
- Gibt eine ConnectorRule zurück, die die Shape-ID und die Verbindung enthält, die mit dem Shape verbunden sind

{{< highlight "java" >}}
ConnectorRule rule= shape.GetConnectorRule();
{{< /highlight >}}

### **Fügt IsSavingCustomLinePattern in SVGSaveOptions hinzu**
- Legt fest, ob benutzerdefiniertes Linienmuster gespeichert wird.

{{< highlight "java" >}}
var opt = new SVGSaveOptions()
{
     IsSavingCustomLinePattern = false
};
{{< /highlight >}}

### **Fügt StreamProvider in XAMLSaveOptions hinzu**
- Ruft den IStreamProvider zum Exportieren von Objekten ab oder legt diesen fest

{{< highlight "java" >}}
MemoryStream stream = new MemoryStream();
var saveOptions = new XAMLSaveOptions();
var streamProvider = new XamlExportStreamProvider(".vsdx");
saveOptions.StreamProvider = streamProvider;
diagram.Save(stream, saveOptions);
{{< /highlight >}}