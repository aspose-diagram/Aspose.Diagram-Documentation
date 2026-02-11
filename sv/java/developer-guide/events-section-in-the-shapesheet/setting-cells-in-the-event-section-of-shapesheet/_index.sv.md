---
title: Ställa in celler i händelsesektionen i ShapeSheet
type: docs
weight: 10
url: /sv/java/setting-cells-in-the-event-section-of-shapesheet/
---
{{% alert color="primary" %}} 

Med hjälp av Aspose.Diagram API kan utvecklare definiera hur en form svarar på specifika användaråtgärder genom att skriva Visio formler som hanterar händelser automatiskt. Närhelst användaren utför en av de åtgärder som beskrivs nedan, utvärderas formeln i motsvarande ShapeSheet-cell.

- **Texten** - Ett händelseelement som utvärderas när en forms text eller textkomposition ändras.
- **EventXFMod** - Formens position, storlek eller orientering på sidan ändras.
- **EventDblKlick** - Formen är dubbelklickad.
- **EventDrop** En ny instans skapas genom att klistra in, duplicera eller dra en form, eller genom att dra och släppa en mall.
- **EventMultiDrop** - när flera nya instanser skapas genom att klistra in, duplicera eller dra en form, eller genom att dra och släppa en mall.
- **Uppgifterna** - Reserverad för framtida bruk.

{{% /alert %}} 
## **Ställa in händelseceller**
[Händelse](https://reference.aspose.com/diagram/java/com.aspose.diagram/event) klass tillåter utvecklare att ställa in händelseceller i ShapeSheet. Det här hjälpämnet visar hur utvecklare kan ställa in formler i händelsecellerna:


{{< highlight java >}}
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

