---
title: Arbeiten mit dem Geometrieabschnitt
type: docs
weight: 190
url: /de/net/working-with-geometry-section/
description: In diesem Abschnitt wird erläutert, wie Sie die Geometrie von Visio mithilfe von Aspose.Diagram erhalten
---
## **Abschnitt "Konnektorgeometrie" im ShapeSheet bearbeiten**
Jede Form in Microsoft Office Visio besteht aus einer oder mehreren „Geometrien“. Jede Geometrie repräsentiert eine andere Komponente der Form. Die meisten Formen haben nur eine Geometrie, aber einige haben zwei oder mehr. Aspose.Diagram APIs ermöglichen Entwicklern, diese Geometrien programmgesteuert zu verwalten.
### **Programmierbeispiel**
Die folgenden Codeausschnitte verwalten Geometrien einer Form.


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

