---
title: Impostazione delle celle nella sezione Event di ShapeSheet
type: docs
weight: 10
url: /it/net/setting-cells-in-the-event-section-of-shapesheet/
description: Gestisci le proprietà degli eventi dei file visio.
---
{{% alert color="primary" %}} 

Utilizzando Aspose.Diagram API, gli sviluppatori possono definire in che modo una forma risponde a specifiche azioni dell'utente scrivendo formule Visio che gestiscono automaticamente gli eventi. Ogni volta che l'utente esegue una delle quattro azioni descritte di seguito, viene valutata la formula nella cella ShapeSheet corrispondente.

- **Il testo** - Un elemento evento che viene valutato quando il testo di una forma o la composizione del testo cambiano.
- **EventoXFMod** - La posizione, le dimensioni o l'orientamento della forma sulla pagina viene modificata.
- **EventDblClick** - Si fa doppio clic sulla forma.
- **EventDrop** Una nuova istanza viene creata incollando, duplicando o trascinando una forma o trascinando e rilasciando un master.
- **EventoMultiDrop** - quando vengono create più nuove istanze incollando, duplicando o trascinando una forma o trascinando e rilasciando un master.
- **I dati** - Riservato per uso futuro.

{{% /alert %}} 
## **Impostazione delle celle degli eventi**
[Evento](https://reference.aspose.com/diagram/net/aspose.diagram/event) class consente agli sviluppatori di impostare le celle degli eventi in ShapeSheet. Questo argomento della guida mostra come gli sviluppatori possono impostare le formule nelle celle degli eventi:


{{< highlight csharp >}}
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

