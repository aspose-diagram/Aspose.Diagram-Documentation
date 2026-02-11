---
title: Travailler avec la section Géométrie
type: docs
weight: 190
url: /fr/net/working-with-geometry-section/
description: Cette section explique comment obtenir la géométrie de Visio en utilisant Aspose.Diagram
---
## **Modifier la section de géométrie du connecteur dans la feuille ShapeSheet**
Toute forme dans Microsoft Office Visio est composée d'une ou plusieurs "géométries". Chaque géométrie représente un composant différent de la forme. La plupart des formes n'ont qu'une seule géométrie, mais certaines en ont deux ou plus. Les API Aspose.Diagram permettent aux développeurs de gérer ces géométries par programmation.
### **Exemple de programmation**
Les extraits de code ci-dessous gèrent les géométries d'une forme.


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

