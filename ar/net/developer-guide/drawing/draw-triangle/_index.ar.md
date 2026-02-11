---
title: ارسم المثلث
type: docs
weight: 60
url: /ar/net/drawing/draw-triangle
description: يشرح هذا القسم كيفية رسم المثلث في صفحة visio باستخدام Aspose.Diagram. الدعم باستخدام C# لرسم المثلث وحفظه بصيغة pdf و svg و html و image و xps وتنسيقات أخرى.
---
## **ارسم المثلث في Visio**
Aspose.Diagram for .NET API يسمح للمطورين برسم شكل مثلث في الصفحة. يوضح مثال الكود أدناه كيفية رسم مثلث في رسم Visio.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Initiazlie a new PointF[]
PointF[] ps = new PointF[] { new PointF(1, 1), new PointF(5, 1), new PointF(3, 4.464f), new PointF(1, 1) };
//Draw Triangle in page
diagram.Pages[0].DrawPolyline(1, 1, 2, 2, ps);

// Save diagram
diagram.Save(dataDir + "DrawTriangleInPage_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```

## **ارسم المثلث في SVG**
Aspose.Diagram for .NET API يسمح للمطورين برسم مثلث في الصفحة وحفظه بتنسيق SVG. يوضح مثال الكود أدناه كيفية رسم مثلث في رسم Visio وحفظه بتنسيق SVG.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Initiazlie a new PointF[]
PointF[] ps = new PointF[] { new PointF(1, 1), new PointF(5, 1), new PointF(3, 4.464f), new PointF(1, 1) };
//Draw Triangle in page
diagram.Pages[0].DrawPolyline(1, 1, 2, 2, ps);

// Save diagram as SVG images
SVGSaveOptions imageSaveOptions = new SVGSaveOptions();
imageSaveOptions.PageIndex = 0;
diagram.Save(dataDir + "DrawTriangleInPage_out.svg", imageSaveOptions);

{{< /highlight >}}
```

## **ارسم المثلث في PDF**
Aspose.Diagram for .NET API يسمح للمطورين برسم مثلث في الصفحة وحفظه بتنسيق PDF. يوضح مثال الكود أدناه كيفية رسم مثلث في رسم Visio وحفظه بتنسيق PDF.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Initiazlie a new PointF[]
PointF[] ps = new PointF[] { new PointF(1, 1), new PointF(5, 1), new PointF(3, 4.464f), new PointF(1, 1) };
//Draw Triangle in page
diagram.Pages[0].DrawPolyline(1, 1, 2, 2, ps);

// Save diagram
diagram.Save(dataDir + "DrawTriangleInPage_out.pdf", new PdfSaveOptions());

{{< /highlight >}}
```

## **ارسم المثلث في PNG**
Aspose.Diagram for .NET API يسمح للمطورين برسم مثلث في الصفحة وحفظه بتنسيق PNG. يوضح مثال الكود أدناه كيفية رسم مثلث في رسم Visio وحفظه بتنسيق PNG.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Initiazlie a new PointF[]
PointF[] ps = new PointF[] { new PointF(1, 1), new PointF(5, 1), new PointF(3, 4.464f), new PointF(1, 1) };
//Draw Triangle in page
diagram.Pages[0].DrawPolyline(1, 1, 2, 2, ps);

// Save diagram as PNG image
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFileFormat.PNG);
imageSaveOptions.PageIndex = 0;
diagram.Save(dataDir + "DrawTriangleInPage_out.png", imageSaveOptions);

{{< /highlight >}}
```

## **ارسم المثلث في HTML**
Aspose.Diagram for .NET API يسمح للمطورين برسم مثلث في الصفحة وحفظه بتنسيق HTML. يوضح مثال الكود أدناه كيفية رسم مثلث في رسم Visio وحفظه بتنسيق HTML.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Initiazlie a new PointF[]
PointF[] ps = new PointF[] { new PointF(1, 1), new PointF(5, 1), new PointF(3, 4.464f), new PointF(1, 1) };
//Draw Triangle in page
diagram.Pages[0].DrawPolyline(1, 1, 2, 2, ps);

// Save diagram
diagram.Save(dataDir + "DrawTriangleInPage_out.html", new HTMLSaveOptions());

{{< /highlight >}}
```
