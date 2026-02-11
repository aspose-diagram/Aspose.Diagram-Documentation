---
title: Arbeta med Geometri Sektion
type: docs
weight: 190
url: /sv/net/working-with-geometry-section/
description: Det här avsnittet förklarar hur man får geometrin för Visio med Aspose.Diagram
---
## **Redigera Connector Geometry Section i ShapeSheet**
Vilken form som helst i Microsoft Office Visio är sammansatt av en eller flera "geometrier". Varje geometri representerar en annan komponent i formen. De flesta former har bara en geometri, men vissa har två eller fler. Aspose.Diagram API:er tillåter utvecklare att hantera dessa geometrier programmatiskt.
### **Programmeringsexempel**
Kodavsnitten nedan hanterar en forms geometrier.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_GeometrySection();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Set connector shape by page name and ID
long connectorId = 4;
Shape connector = diagram.Pages.GetPage("Page-1").Shapes.GetShape(connectorId);
// Get connector geometry at index 0
LineTo defaultLineTo = connector.Geoms[0].CoordinateCol.LineToCol[0];
// Remove connector geometry from index 0
connector.Geoms[0].CoordinateCol.LineToCol[0].Del = BOOL.True;

// Initialize LineTo geometry object
LineTo lineTo = new LineTo();
// Set X value
lineTo.X.Value = 0;
// Set Y value
lineTo.Y.Value = defaultLineTo.Y.Value / 2;
// Add connector geometry
connector.Geoms[0].CoordinateCol.Add(lineTo);

// Initialize LineTo geometry object
lineTo = new LineTo();
// Set Y value
lineTo.Y.Value = defaultLineTo.Y.Value / 2;
// Set X value
lineTo.X.Value = defaultLineTo.X.Value;
// Add connector geometry
connector.Geoms[0].CoordinateCol.Add(lineTo);

// Initialize LineTo geometry object
lineTo = new LineTo();
// Set X value
lineTo.X.Value = defaultLineTo.X.Value;
// Set Y value
lineTo.Y.Value = defaultLineTo.Y.Value;
// Add connector geometry
connector.Geoms[0].CoordinateCol.Add(lineTo);

// Save diagram in VDX format
diagram.Save(dataDir + "EditConnectorGeometry_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

