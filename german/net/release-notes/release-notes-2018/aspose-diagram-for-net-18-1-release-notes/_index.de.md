---
title: Aspose.Diagram for .NET 18.1 Versionshinweise
type: docs
weight: 120
url: /de/net/aspose-diagram-for-net-18-1-release-notes/
---
{{% alert color="primary" %}} 

 Diese Seite enthält Versionshinweise für[Aspose.Diagram for .NET 18.1](https://www.nuget.org/packages/Aspose.Diagram/18.1.0).

{{% /alert %}} 
## **Verbesserungen und Änderungen**

|**Taste**|**Zusammenfassung**|**Kategorie**|
|:- |:- |:- |
|DIAGRAMNET-50494|Unterstützung zum Duplizieren / Klonen einer diagram-Seite hinzufügen|Erweiterung|
|DIAGRAMNET-51057|Die Befehlsschaltfläche fehlt nach dem Entfernen einer Seite aus VSDM|Erweiterung|
|DIAGRAMNET-51422|VSDX zu PDF - die Schatten werden bei Prozessformen ignoriert|Erweiterung|
|DIAGRAMNET-50467|VSD in PDF-Konvertierung, das Firmenlogo ist falsch platziert|Insekt|
|DIAGRAMNET-50469|VSD in PDF-Konvertierung, der Radioformtext ist etwas höher als gewöhnlich|Insekt|
|DIAGRAMNET-51199|Titeltext wird beim Speichern von VSDM in SVG nicht ausgerichtet|Insekt|
|DIAGRAMNET-51388|Probleme beim Laden und Speichern von vsdx-Dateien|Insekt|
|DIAGRAMNET-51398|VSD zu PNG - die Textposition ist falsch|Insekt|
|DIAGRAMNET-51407|VSD zu JPEG - die Textelemente sind falsch platziert|Insekt|
|DIAGRAMNET-51419|Die Größe von Formen wird in der Datei vsdx nicht richtig geändert|Insekt|
|DIAGRAMNET-51420|VSDX Datei wird nach dem Laden und Speichern beschädigt|Insekt|
|DIAGRAMNET-51421|VSDX zu PDF - falsche Schriftfarbe des Textes|Insekt|
## **Öffentliche API und rückwärts inkompatible Änderungen**
Im Folgenden finden Sie eine Liste aller Änderungen, die an der öffentlichen API vorgenommen wurden, z. B. hinzugefügte, umbenannte, entfernte oder veraltete Mitglieder, sowie alle nicht abwärtskompatiblen Änderungen, die an Aspose.Diagram for .NET vorgenommen wurden. Wenn Sie Bedenken zu einer der aufgeführten Änderungen haben, äußern Sie diese bitte das[Aspose.Diagram Support-Forum](https://forum.aspose.com/c/diagram/17).
### **Fügt Copy-Member in der Page-Klasse hinzu**
Das Copy-Member nimmt eine Zielseiteninstanz als Parameter, um diese Seite zu klonen.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page(1);

// copy diagram

newPage.Copy(diagram.Pages[0]);

{{< /highlight >}}
### **Anwendungsbeispiele**
Bitte überprüfen Sie die Liste der Hilfethemen, die in den Aspose.Diagram-Wiki-Dokumenten hinzugefügt wurden:

1. [Kopieren Sie die Seite Visio in eine andere Seiteninstanz](https://docs.aspose.com/diagram/net/retrieve-get-copy-and-insert-a-page/#copy-visio-page-to-another-page-instance)
