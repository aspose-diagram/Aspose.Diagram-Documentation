---
title: Aspose.Diagram for .NET 17.8 Versionshinweise
type: docs
weight: 50
url: /de/net/aspose-diagram-for-net-17-8-release-notes/
---
{{% alert color="primary" %}} 

 Diese Seite enthält Versionshinweise für[Aspose.Diagram for .NET 17.8](https://www.nuget.org/packages/Aspose.Diagram/17.8.0).

{{% /alert %}} 
## **Verbesserungen und Änderungen**

|**Taste**|**Zusammenfassung**|**Kategorie**|
|:- |:- |:- |
|DIAGRAMNET-51295|VSDX zu SVG - die niedrige Qualität der SVG-Ausgabe.|Erweiterung|
|DIAGRAMNET-51298|SVGSaveOptions - fügt Unterstützung hinzu, um den Grad der Bitmap-Komprimierung zu steuern.|Erweiterung|
|DIAGRAMNET-51300|Fügen Sie Unterstützung für verbindende Formen mit Verbindungsindex hinzu.|Erweiterung|
|DIAGRAMNET-50577|VSDX in PDF-Konvertierung, der Text der Kreisform ist falsch platziert - I.|Insekt|
|DIAGRAMNET-50582|VSDX zur HTML-Konvertierung, der Text der Kreisform ist falsch platziert - I.|Insekt|
|DIAGRAMNET-50601|VSDX in PDF-Konvertierung, der Text der Kreisform ist falsch platziert - II.|Insekt|
|DIAGRAMNET-50606|VSDX zur HTML-Konvertierung, der Text der Kreisform ist falsch platziert - II.|Insekt|
|DIAGRAMNET-51197|Warndreieckformen werden beim Speichern von VSDM als SVG nicht korrekt gerendert.|Insekt|
|DIAGRAMNET-51245|Verdrängte Textelemente beim Konvertieren einer VSD in PDF.|Insekt|
|DIAGRAMNET-51246|Beim Konvertieren von VSD in PDF wurden falsche Schriftarten auf Text angewendet.|Insekt|
|DIAGRAMNET-51296|VSDM zu SVG - das Bild wird abgeschnitten.|Insekt|
|DIAGRAMNET-51301|VSDX zu PDF - Textfarbe auf Verbindungslinien wird geändert.|Insekt|
|DIAGRAMNET-51302|VSDX nach PDF - fehlende Grafikelemente.|Insekt|
|DIAGRAMNET-51304|VSDX in PDF - unvollständige Darstellung des Flussdiagramms.|Insekt|
|DIAGRAMNET-51305|VSDX nach PDF - fehlende Grafikelemente.|Insekt|
|DIAGRAMNET-51306|VSDX zu PDF - Textfarbe auf Verbindungslinien wird geändert.|Insekt|
|DIAGRAMNET-51307|VSDX nach PDF - fehlende Grafikelemente.|Insekt|
|DIAGRAMNET-51313|Die Routine zum Öffnen und Speichern einer VSDX-Zeichnung generiert eine beschädigte Ausgabedatei.|Insekt|
|DIAGRAMNET-51314|VSDX zu SVG - falsche Positionierung des Textes.|Insekt|
|DIAGRAMNET-51317|VSDX nach PDF - der Text der Verbindungslinien fehlt.|Insekt|
|DIAGRAMNET-51318|VSDX zu PDF - der fett formatierte Text von Rechteckformen fehlt.|Insekt|
|DIAGRAMNET-51319|VSDM an SVG - Die arithmetische Operation führte zu einem Überlauffehler.|Insekt|
|DIAGRAMNET-51320|Fehler im Formelement beim Laden von VSDM.|Insekt|
|DIAGRAMNET-51323|VSDM nach SVG - alle Verbindungsleitungen fehlen.|Insekt|
|DIAGRAMNET-51324|VSDM zu SVG - falscher Rahmenstil und Rahmenfarbe verschiedener Formen.|Insekt|
|DIAGRAMNET-51326|Problem nach dem Hinzufügen von zwei Kommentaren zur Form.|Insekt|
|DIAGRAMNET-51327|Problem nach Verwendung der „AddComment“-Methode beim Hinzufügen von Kommentaren zu verschiedenen Shapes.|Insekt|
|DIAGRAMNET-51328|Aspose Diagram importiert die Form fälschlicherweise in das Dokument.|Insekt|
|DIAGRAMNET-51330|VSDM zu SVG - ein zusätzlicher Wasserzeichentext wird hinzugefügt.|Insekt|
|DIAGRAMNET-51332|VSDM zu SVG - falsche Darstellung eines Symbols.|Insekt|
|DIAGRAMNET-51334|VSDM zu SVG - verschobener Text in der oberen rechten Ecke.|Insekt|
|DIAGRAMNET-51335|VSDM zu SVG - falsche Darstellung des Hintergrundbilds.|Insekt|
|DIAGRAMNET-51337|VSD zu HTML – ungültiges Format der Eingabezeichenfolge.|Insekt|
## **Öffentliche API und rückwärts inkompatible Änderungen**
Im Folgenden finden Sie eine Liste aller Änderungen, die an der öffentlichen API vorgenommen wurden, z. B. hinzugefügte, umbenannte, entfernte oder veraltete Mitglieder, sowie alle nicht abwärtskompatiblen Änderungen, die an Aspose.Diagram for .NET vorgenommen wurden. Wenn Sie Bedenken zu einer der aufgeführten Änderungen haben, äußern Sie diese bitte das[Aspose.Diagram Support-Forum](https://forum.aspose.com/c/diagram/17).
### **Fügt ein Quality-Mitglied in der SVGSaveOptions-Klasse hinzu**
Es erhält oder setzt einen Wert, der die Qualität der erzeugten Bilder bestimmt.

{{< highlight "java" >}}

 string dataDir = @"c:\temp\";

// Load an existing drawing

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// specify SVG export settings

SVGSaveOptions options = new SVGSaveOptions();

// set image quality

options.Quality = 100;

// save drawing in the SVG format

diagram.Save(dataDir + "UseSVGSaveOptions_out.svg", options);

{{< /highlight >}}
### **Fügt die ConnectShapesViaConnectorIndex-Methode in der Page-Klasse hinzu**
Es ermöglicht das Verbinden von Formen mithilfe von Verbindungsindizes.

{{< highlight "java" >}}

 string dataDir = @"c:\temp\";

// Load an existing drawing

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get shapes by ID

Aspose.Diagram.Shape shape1 = diagram.Pages[0].Shapes.GetShape(1);

Aspose.Diagram.Shape shape2 = diagram.Pages[0].Shapes.GetShape(2);

// add connector shapes

Aspose.Diagram.Shape connector1 = new Aspose.Diagram.Shape();

long connecter1Id = diagram.AddShape(connector1, "Dynamic connector", 0);

// connect shapes by index of conneecting points

diagram.Pages[0].ConnectShapesViaConnectorIndex(shape1.ID, 6, shape2.ID, 3, connecter1Id);

// save drawing

diagram.Save(dataDir + "UseSVGSaveOptions_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **Anwendungsbeispiele**
Bitte überprüfen Sie die Liste der Hilfethemen, die in den Aspose.Diagram-Wiki-Dokumenten hinzugefügt wurden:

1. [Verwenden Sie Verbindungsindizes, um Shapes zu verbinden](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/#use-connection-indexes-to-connect-shapes)
1. [Verwendung der SVG-Speicheroptionen](https://docs.aspose.com/diagram/net/save-visio-document/)
