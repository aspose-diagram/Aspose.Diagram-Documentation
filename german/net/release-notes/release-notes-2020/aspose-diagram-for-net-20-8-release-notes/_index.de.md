---
title: Aspose.Diagram for .NET 20.8 Versionshinweise
type: docs
weight: 14
url: /de/net/aspose-diagram-for-net-20-8-release-notes/
---
{{% alert color="primary" %}}

Diese Seite enthält Versionshinweise für Aspose.Diagram for .NET 20.8.

{{% /alert %}}
## **Verbesserungen und Änderungen**  ##

|**Taste**|**Zusammenfassung**|**Kategorie**|
|:- |:- |:- |
|DIAGRAMNET-51886|Erstellen Sie die Möglichkeit, Ole-Objekte wie Wörter, Zellen, Folien usw. in die Diagram in die einzelne Form einzufügen, die sowohl Objektdaten als auch ein Vorschaubild enthält.|Erweiterung|
|DIAGRAMNET-51888|Visio in PDF - API braucht lange für die Konvertierung|Erweiterung|
|DIAGRAMNET-51889|Speichern in einer PDF-Schleife von mehr als 20 Minuten|Erweiterung|
|DIAGRAMNET-51893|Fehlendes viewBox-Attribut nach Konvertierung von VSDX in SVG|Erweiterung|
|DIAGRAMNET-51851|VSDX in PDF - einige Symbole fehlen und einige werden nicht richtig gerendert|Insekt|
|DIAGRAMNET-51873|VSDX in PDF - Inhalt wird im Ausgabe-PDF links angezeigt|Insekt|
|DIAGRAMNET-51874|VSDX nach PDF - Inhalt und Zeilen fehlen in der Ausgabe|Insekt|
|DIAGRAMNET-51876|VSDX zu PNG - einige Formen sind in der Ausgabe falsch|Insekt|
|DIAGRAMNET-51879|Visio nach PDF - Ausgabe ist nicht korrekt|Insekt|
|DIAGRAMNET-51894|System.NullReferenceException beim Laden von diagram|Insekt|
|DIAGRAMNET-51895|Gruppeneigenschaftsdaten wie SelectionModel, DisplayMode können nicht abgerufen werden|Insekt|

## **Öffentliche API und rückwärtsinkompatible Änderungen**  ##
Im Folgenden finden Sie eine Liste aller Änderungen, die an der öffentlichen API vorgenommen wurden, z. B. hinzugefügte, umbenannte, entfernte oder veraltete Mitglieder, sowie alle nicht abwärtskompatiblen Änderungen, die an Aspose.Diagram for .NET vorgenommen wurden das Aspose.Diagram Support-Forum.

####  Methode AddShape in Seite hinzugefügt ####
```
Diagram diagram = new Diagram();

// Get page object by index
Aspose.Diagram.Page page0 = diagram.Pages[0];
// set pinX, pinY, width and height
double pinX = 2, pinY = 2, width = 4, hieght = 3;

// Import ole as Visio shape word
page0.AddShape(pinX, pinY, width, hieght, new FileStream( "imageword.emf", FileMode.OpenOrCreate), new FileStream( "wordsource.doc", FileMode.OpenOrCreate));
```
