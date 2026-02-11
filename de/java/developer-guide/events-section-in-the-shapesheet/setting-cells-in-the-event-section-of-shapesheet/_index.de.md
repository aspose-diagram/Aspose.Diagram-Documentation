---
title: Festlegen von Zellen im Ereignisabschnitt von ShapeSheet
type: docs
weight: 10
url: /de/java/setting-cells-in-the-event-section-of-shapesheet/
---
{{% alert color="primary" %}} 

Mit Aspose.Diagram API können Entwickler definieren, wie eine Form auf bestimmte Benutzeraktionen reagiert, indem sie Visio-Formeln schreiben, die Ereignisse automatisch verarbeiten. Immer wenn der Benutzer eine der unten beschriebenen Aktionen ausführt, wird die Formel in der entsprechenden ShapeSheet-Zelle ausgewertet.

- **Der Text** - Ein Ereigniselement, das ausgewertet wird, wenn sich der Text oder die Textkomposition einer Form ändert.
- **EventXFMod** - Die Position, Größe oder Ausrichtung der Form auf der Seite wird geändert.
- **EventDblClick** - Die Form wird doppelt angeklickt.
- **EventDrop** Eine neue Instanz wird durch Einfügen, Duplizieren oder Ziehen einer Form oder durch Ziehen und Ablegen eines Masters erstellt.
- **EventMultiDrop** - wenn mehrere neue Instanzen durch Einfügen, Duplizieren oder Ziehen einer Form oder durch Ziehen und Ablegen eines Masters erstellt werden.
- **Die Daten** - Reserviert für zukünftige Verwendung.

{{% /alert %}} 
## **Festlegen von Ereigniszellen**
[Vorfall](https://reference.aspose.com/diagram/java/com.aspose.diagram/event) -Klasse ermöglicht es Entwicklern, Ereigniszellen im ShapeSheet festzulegen. Dieses Hilfethema zeigt, wie Entwickler Formeln in den Ereigniszellen festlegen können:

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SettingEventCells.class);
// load diagram
Diagram diagram = new Diagram(dataDir + "TestTemplate.vsdm");
// get page
Page page = diagram.getPages().get(0);
// get shape id
long shapeId = page.addShape(3.0, 3.0, 0.36, 0.36, "Square");
// get shape
Shape shape = page.getShapes().getShape(shapeId);

// set event cells in the ShapeSheet
shape.getEvent().getEventXFMod().getUfe().setF("CALLTHIS(\"ThisDocument.ShowAlert\")");
shape.getEvent().getEventXFMod().getUfe().setF("CALLTHIS(\"ThisDocument.ShowAlert\")");
shape.getEvent().getEventXFMod().getUfe().setF("CALLTHIS(\"ThisDocument.ShowAlert\")");
shape.getEvent().getEventXFMod().getUfe().setF("CALLTHIS(\"ThisDocument.ShowAlert\")");
shape.getEvent().getEventXFMod().getUfe().setF("CALLTHIS(\"ThisDocument.ShowAlert\")");
shape.getEvent().getEventXFMod().getUfe().setF("CALLTHIS(\"ThisDocument.ShowAlert\")");

// save diagram
diagram.save(dataDir + "Output_NET.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}
```
