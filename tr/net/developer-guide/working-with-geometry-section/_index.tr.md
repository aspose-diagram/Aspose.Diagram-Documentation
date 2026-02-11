---
title: Geometri Kesiti ile Çalışma
type: docs
weight: 190
url: /tr/net/working-with-geometry-section/
description: Bu bölümde Aspose.Diagram kullanılarak Visio geometrisinin nasıl elde edileceği açıklanmaktadır.
---
## **ShapeSheet'te Bağlayıcı Geometri Bölümünü Düzenle**
Microsoft Office Visio'deki herhangi bir şekil, bir veya daha fazla "geometriden" oluşur. Her geometri, şeklin farklı bir bileşenini temsil eder. Çoğu şeklin yalnızca bir geometrisi vardır, ancak bazılarının iki veya daha fazla geometrisi vardır. Aspose.Diagram API'ler, geliştiricilerin bu geometrileri programlı olarak yönetmesine olanak tanır.
### **Programlama Örneği**
Aşağıdaki kod parçacıkları, bir Şeklin geometrilerini yönetir.


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

