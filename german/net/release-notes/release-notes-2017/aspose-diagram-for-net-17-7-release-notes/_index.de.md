---
title: Aspose.Diagram for .NET 17.7 Versionshinweise
type: docs
weight: 60
url: /de/net/aspose-diagram-for-net-17-7-release-notes/
---
{{% alert color="primary" %}} 

 Diese Seite enthält Versionshinweise für[Aspose.Diagram for .NET 17.7](https://www.nuget.org/packages/Aspose.Diagram/17.7.0).

{{% /alert %}} 
## **Verbesserungen und Änderungen**

|**Taste**|**Zusammenfassung**|**Kategorie**|
|:- |:- |:- |
|DIAGRAMNET-51204|Das Druckerpapierformat wird nach dem Speichern von diagram geändert.|Erweiterung|
|DIAGRAMNET-51230|Falsche Werte der Seitenränder.|Erweiterung|
|DIAGRAMNET-51274|Fügen Sie Unterstützung für das Einfügen von Kommentaren auf Formebene hinzu.|Erweiterung|
|DIAGRAMNET-51297|Eingabe VDX - falsches Lesen von SolutionXML.|Erweiterung|
|DIAGRAMNET-51061|Fehlende Formen beim Konvertieren einer VST in PNG.|Insekt|
|DIAGRAMNET-51262|Verdrängte Textelemente beim Konvertieren einer VSDM in SVG.|Insekt|
|DIAGRAMNET-51276|VSD zu SVG - alle Symbole sind nicht richtig sichtbar.|Insekt|
|DIAGRAMNET-51277|VSDM bis SVG - Fehlender Schatten von Formen.|Insekt|
|DIAGRAMNET-51279|Ein fehlendes Zeichen beim Konvertieren einer VSD in PDF.|Insekt|
|DIAGRAMNET-51282|Einige vdx-Dateien sind nach dem Speichern beschädigt.|Insekt|
|DIAGRAMMNETZ-51284-|DiagramException tritt beim Laden der Datei vsdx auf.|Insekt|
|DIAGRAMNET-51285|VSD bis PNG - alle Textelemente fehlen.|Insekt|
|DIAGRAMNET-51286|VSD in PNG - die teilweise Wiedergabe einer Form.|Insekt|
|DIAGRAMNET-51288|Ungültiger Farbwertfehler beim Konvertieren von VSDX in PNG.|Insekt|
|DIAGRAMNET-51289|Das Kommentarsymbol auf Seitenebene zeigt keinen Text an.|Insekt|
|DIAGRAMNET-51290|Aspose.Diagram Fehler in Methode SetWidth.|Insekt|
|DIAGRAMNET-51291|Ausgabe VSDX - falsches Layout beim gerade setzen der Verbindungslinien.|Insekt|
|DIAGRAMNET-51292|Ausgabe VSDX - Das Textelement der Verbindungslinien ist falsch platziert.|Insekt|
|DIAGRAMNET-51293|VSDX zu SVG - eine zusätzliche Markierung erscheint zusammen mit Formen.|Insekt|
|DIAGRAMNET-51294|VSDM zu SVG - eine zusätzliche Markierung erscheint zusammen mit Formen.|Insekt|
## **Öffentliche API und rückwärts inkompatible Änderungen**
Im Folgenden finden Sie eine Liste aller Änderungen, die an der öffentlichen API vorgenommen wurden, z. B. hinzugefügte, umbenannte, entfernte oder veraltete Mitglieder, sowie alle nicht abwärtskompatiblen Änderungen, die an Aspose.Diagram for .NET vorgenommen wurden. Wenn Sie Bedenken zu einer der aufgeführten Änderungen haben, äußern Sie diese bitte das[Aspose.Diagram Support-Forum](https://forum.aspose.com/c/diagram/17).
### **AddComment-Methode wird in der Page-Klasse hinzugefügt**
Eine überladene AddComment-Methode, die von der Page-Klasse bereitgestellt wird, akzeptiert eine Shape-Klasseninstanz und eine Textzeichenfolge des Kommentars.

{{< highlight "java" >}}

 // load diagram

Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

// retrieve page by name

Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// retrieve shape by ID

Aspose.Diagram.Shape shape = page.Shapes.GetShape(12);

page.AddComment(shape, "Hello");

// save diagram

diagram.Save(@"c:\temp\Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **Anwendungsbeispiele**
Bitte überprüfen Sie die Liste der Hilfethemen, die in den Aspose.Diagram-Wiki-Dokumenten hinzugefügt wurden:

1. [Fügen Sie in der Zeichnung Visio einen Kommentar auf Formebene hinzu](/diagram/de/net/working-with-comments/#workingwithcomments-addashape-levelcommentinvisiodrawing)
