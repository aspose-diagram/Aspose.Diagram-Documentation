---
title: ارسم الماس
type: docs
weight: 30
url: /ar/net/drawing/draw-diamond
description: يشرح هذا القسم كيفية رسم الماس في صفحة visio باستخدام Aspose.Diagram. الدعم باستخدام C# لرسم الماس وحفظه بتنسيق pdf و svg و html و image و xps وتنسيقات أخرى.
---
## **ارسم الماس في Visio**
Aspose.Diagram for .NET API يسمح للمطورين برسم شكل ماسي في الصفحة. يوضح مثال الكود أدناه كيفية رسم ماسة في رسم Visio.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Initiazlie a new PointF[]
PointF[] ps = new PointF[] { new PointF(1, 2), new PointF(2, 0), new PointF(3, 2), new PointF(2, 4), new PointF(1, 2) };
//Draw Diamond in page
diagram.Pages[0].DrawPolyline(1, 1, 2, 2, ps);

// Save diagram
diagram.Save(dataDir + "DrawDiamondInPage_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```

## **ارسم الماس في SVG**
Aspose.Diagram for .NET API يسمح للمطورين برسم ماسة في الصفحة وحفظها بتنسيق SVG. يوضح مثال الكود أدناه كيفية رسم ماسة برسم Visio وحفظها بتنسيق SVG.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Initiazlie a new PointF[]
PointF[] ps = new PointF[] { new PointF(1, 2), new PointF(2, 0), new PointF(3, 2), new PointF(2, 4), new PointF(1, 2) };
//Draw Diamond in page
diagram.Pages[0].DrawPolyline(1, 1, 2, 2, ps);

// Save diagram as SVG images
SVGSaveOptions imageSaveOptions = new SVGSaveOptions();
imageSaveOptions.PageIndex = 0;
diagram.Save(dataDir + "DrawDiamondInPage_out.svg", imageSaveOptions);

{{< /highlight >}}
```

## **ارسم الماس في PDF**
Aspose.Diagram for .NET API يسمح للمطورين برسم ماسة في الصفحة وحفظها بتنسيق PDF. يوضح مثال الكود أدناه كيفية رسم ماسة برسم Visio وحفظها بتنسيق PDF.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Initiazlie a new PointF[]
PointF[] ps = new PointF[] { new PointF(1, 2), new PointF(2, 0), new PointF(3, 2), new PointF(2, 4), new PointF(1, 2) };
//Draw Diamond in page
diagram.Pages[0].DrawPolyline(1, 1, 2, 2, ps);

// Save diagram
diagram.Save(dataDir + "DrawDiamondInPage_out.pdf", new PdfSaveOptions());

{{< /highlight >}}
```

## **ارسم الماس في PNG**
Aspose.Diagram for .NET API يسمح للمطورين برسم ماسة في الصفحة وحفظها بتنسيق PNG. يوضح مثال الكود أدناه كيفية رسم ماسة برسم Visio وحفظها بتنسيق PNG.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Initiazlie a new PointF[]
PointF[] ps = new PointF[] { new PointF(1, 2), new PointF(2, 0), new PointF(3, 2), new PointF(2, 4), new PointF(1, 2) };
//Draw Diamond in page
diagram.Pages[0].DrawPolyline(1, 1, 2, 2, ps);

// Save diagram as PNG image
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFileFormat.PNG);
imageSaveOptions.PageIndex = 0;
diagram.Save(dataDir + "DrawDiamondInPage_out.png", imageSaveOptions);

{{< /highlight >}}
```

## **ارسم الماس في HTML**
Aspose.Diagram for .NET API يسمح للمطورين برسم ماسة في الصفحة وحفظها بتنسيق HTML. يوضح مثال الكود أدناه كيفية رسم ماسة برسم Visio وحفظها بتنسيق HTML.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Initiazlie a new PointF[]
PointF[] ps = new PointF[] { new PointF(1, 2), new PointF(2, 0), new PointF(3, 2), new PointF(2, 4), new PointF(1, 2) };
//Draw Diamond in page
diagram.Pages[0].DrawPolyline(1, 1, 2, 2, ps);

// Save diagram
diagram.Save(dataDir + "DrawDiamondInPage_out.html", new HTMLSaveOptions());

{{< /highlight >}}
```
