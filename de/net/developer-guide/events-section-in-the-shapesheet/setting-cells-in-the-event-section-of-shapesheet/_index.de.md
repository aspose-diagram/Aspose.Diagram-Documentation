---
title: Festlegen von Zellen im Ereignisabschnitt von ShapeSheet
type: docs
weight: 10
url: /de/net/setting-cells-in-the-event-section-of-shapesheet/
description: Ereigniseigenschaften von visio-Dateien verwalten.
---
{{% alert color="primary" %}} 

Mit Aspose.Diagram API können Entwickler definieren, wie eine Form auf bestimmte Benutzeraktionen reagiert, indem sie Visio-Formeln schreiben, die Ereignisse automatisch verarbeiten. Immer wenn der Benutzer eine der vier unten beschriebenen Aktionen ausführt, wird die Formel in der entsprechenden ShapeSheet-Zelle ausgewertet.

- **Der Text** - Ein Ereigniselement, das ausgewertet wird, wenn sich der Text oder die Textkomposition einer Form ändert.
- **EventXFMod** - Die Position, Größe oder Ausrichtung der Form auf der Seite wird geändert.
- **EventDblClick** - Die Form wird doppelt angeklickt.
- **EventDrop** Eine neue Instanz wird durch Einfügen, Duplizieren oder Ziehen einer Form oder durch Ziehen und Ablegen eines Masters erstellt.
- **EventMultiDrop** - wenn mehrere neue Instanzen durch Einfügen, Duplizieren oder Ziehen einer Form oder durch Ziehen und Ablegen eines Masters erstellt werden.
- **Die Daten** - Reserviert für zukünftige Verwendung.

{{% /alert %}} 
## **Festlegen von Ereigniszellen**
[Vorfall](https://reference.aspose.com/diagram/net/aspose.diagram/event) -Klasse ermöglicht es Entwicklern, Ereigniszellen im ShapeSheet festzulegen. Dieses Hilfethema zeigt, wie Entwickler Formeln in den Ereigniszellen festlegen können:

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_EventSection();

// Load diagram
Diagram diagram = new Diagram(dataDir + "TestTemplate.vsdm");
// Get page
Aspose.Diagram.Page page = diagram.Pages.GetPage(0);
// Get shape id
long shapeId = page.AddShape(3.0, 3.0, 0.36, 0.36, "Square");
// Get shape
Aspose.Diagram.Shape shape = page.Shapes.GetShape(shapeId);

// Set event cells in the ShapeSheet
shape.Event.EventXFMod.Ufe.F = "CALLTHIS(\"ThisDocument.ShowAlert\")";
shape.Event.EventDblClick.Ufe.F = "CALLTHIS(\"ThisDocument.ShowAlert\")";
shape.Event.EventDrop.Ufe.F = "CALLTHIS(\"ThisDocument.ShowAlert\")";
shape.Event.EventMultiDrop.Ufe.F = "CALLTHIS(\"ThisDocument.ShowAlert\")";
shape.Event.TheText.Ufe.F = "CALLTHIS(\"ThisDocument.ShowAlert\")";
shape.Event.TheData.Ufe.F = "CALLTHIS(\"ThisDocument.ShowAlert\")";

// Save diagram
diagram.Save(dataDir + "SettingCellsInEventSection_out.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}
```
