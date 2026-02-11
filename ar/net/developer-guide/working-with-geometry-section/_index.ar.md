---
title: العمل مع قسم الهندسة
type: docs
weight: 190
url: /ar/net/working-with-geometry-section/
description: يشرح هذا القسم كيفية الحصول على هندسة Visio باستخدام Aspose.Diagram
---
## **قم بتحرير مقطع هندسة الموصل في ورقة الشكل**
أي شكل في Microsoft Office Visio يتكون من واحد أو أكثر من "الأشكال الهندسية". تمثل كل هندسة مكونًا مختلفًا للشكل. تحتوي معظم الأشكال على هندسة واحدة فقط ، لكن بعضها يحتوي على شكلين أو أكثر. تسمح واجهات برمجة التطبيقات Aspose.Diagram للمطورين بإدارة هذه الأشكال الهندسية برمجيًا.
### **عينة البرمجة**
تقوم مقتطفات التعليمات البرمجية أدناه بإدارة الأشكال الهندسية للشكل.


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

