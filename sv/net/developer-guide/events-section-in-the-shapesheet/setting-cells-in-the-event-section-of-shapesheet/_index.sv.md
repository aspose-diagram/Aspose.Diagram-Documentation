---
title: Ställa in celler i händelsesektionen i ShapeSheet
type: docs
weight: 10
url: /sv/net/setting-cells-in-the-event-section-of-shapesheet/
description: Hantera händelseegenskaper för visio-filer.
---
{{% alert color="primary" %}} 

Med hjälp av Aspose.Diagram API kan utvecklare definiera hur en form svarar på specifika användaråtgärder genom att skriva Visio formler som hanterar händelser automatiskt. Närhelst användaren utför en av de fyra åtgärder som beskrivs nedan, utvärderas formeln i motsvarande ShapeSheet-cell.

- **Texten** - Ett händelseelement som utvärderas när en forms text eller textkomposition ändras.
- **EventXFMod** - Formens position, storlek eller orientering på sidan ändras.
- **EventDblKlick** - Formen är dubbelklickad.
- **EventDrop** En ny instans skapas genom att klistra in, duplicera eller dra en form, eller genom att dra och släppa en mall.
- **EventMultiDrop** - när flera nya instanser skapas genom att klistra in, duplicera eller dra en form, eller genom att dra och släppa en mall.
- **Uppgifterna** - Reserverad för framtida bruk.

{{% /alert %}} 
## **Ställa in händelseceller**
[Händelse](https://reference.aspose.com/diagram/net/aspose.diagram/event) klass tillåter utvecklare att ställa in händelseceller i ShapeSheet. Det här hjälpämnet visar hur utvecklare kan ställa in formler i händelsecellerna:


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

