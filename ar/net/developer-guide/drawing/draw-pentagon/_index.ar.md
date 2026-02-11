---
title: ارسم البنتاغون
type: docs
weight: 40
url: /ar/net/drawing/draw-pentagon
description: يشرح هذا القسم كيفية رسم البنتاغون في صفحة visio باستخدام Aspose.Diagram. الدعم باستخدام C# لرسم البنتاغون وحفظه بصيغة pdf و svg و html و image و xps وتنسيقات أخرى.
---
## **ارسم البنتاغون في Visio**
Aspose.Diagram for .NET API يسمح للمطورين برسم شكل خماسي في صفحة يوضح مثال الكود أدناه كيفية رسم خماسي في رسم Visio.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Initiazlie a new PointF[]
PointF[] ps = new PointF[] { new PointF(1, 1), new PointF(2, 1), new PointF(2.309f, 1.951f), new PointF(1.5f, 2.54f), new PointF(0.691f, 1.951f), new PointF(1, 1) };
//Draw Pentagon in page
diagram.Pages[0].DrawPolyline(1, 1, 2, 2, ps);

// Save diagram
diagram.Save(dataDir + "DrawPentagonInPage_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


## **ارسم البنتاغون في SVG**
Aspose.Diagram for .NET API يسمح للمطورين برسم خماسي في الصفحة وحفظه بتنسيق SVG. يوضح مثال الكود أدناه كيفية رسم خماسي في رسم Visio وحفظه بتنسيق SVG.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Initiazlie a new PointF[]
PointF[] ps = new PointF[] { new PointF(1, 1), new PointF(2, 1), new PointF(2.309f, 1.951f), new PointF(1.5f, 2.54f), new PointF(0.691f, 1.951f), new PointF(1, 1) };
//Draw Pentagon in page
diagram.Pages[0].DrawPolyline(1, 1, 2, 2, ps);

// Save diagram as SVG images
SVGSaveOptions imageSaveOptions = new SVGSaveOptions();
imageSaveOptions.PageIndex = 0;
diagram.Save(dataDir + "DrawPentagonInPage_out.svg", imageSaveOptions);

{{< /highlight >}}


## **ارسم البنتاغون في PDF**
Aspose.Diagram for .NET API يسمح للمطورين برسم خماسي في الصفحة وحفظه بتنسيق PDF. يوضح مثال الكود أدناه كيفية رسم خماسي في رسم Visio وحفظه بتنسيق PDF.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Initiazlie a new PointF[]
PointF[] ps = new PointF[] { new PointF(1, 1), new PointF(2, 1), new PointF(2.309f, 1.951f), new PointF(1.5f, 2.54f), new PointF(0.691f, 1.951f), new PointF(1, 1) };
//Draw Pentagon in page
diagram.Pages[0].DrawPolyline(1, 1, 2, 2, ps);

// Save diagram
diagram.Save(dataDir + "DrawPentagonInPage_out.pdf", new PdfSaveOptions());

{{< /highlight >}}


## **ارسم البنتاغون في PNG**
Aspose.Diagram for .NET API يسمح للمطورين برسم خماسي في الصفحة وحفظه بتنسيق PNG. يوضح مثال الكود أدناه كيفية رسم خماسي في رسم Visio وحفظه بتنسيق PNG.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Initiazlie a new PointF[]
PointF[] ps = new PointF[] { new PointF(1, 1), new PointF(2, 1), new PointF(2.309f, 1.951f), new PointF(1.5f, 2.54f), new PointF(0.691f, 1.951f), new PointF(1, 1) };
//Draw Pentagon in page
diagram.Pages[0].DrawPolyline(1, 1, 2, 2, ps);

// Save diagram as PNG image
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFileFormat.PNG);
imageSaveOptions.PageIndex = 0;
diagram.Save(dataDir + "DrawPentagonInPage_out.png", imageSaveOptions);

{{< /highlight >}}


## **ارسم البنتاغون في HTML**
Aspose.Diagram for .NET API يسمح للمطورين برسم خماسي في الصفحة وحفظه بتنسيق HTML. يوضح مثال الكود أدناه كيفية رسم خماسي في رسم Visio وحفظه بتنسيق HTML.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Initiazlie a new PointF[]
PointF[] ps = new PointF[] { new PointF(1, 1), new PointF(2, 1), new PointF(2.309f, 1.951f), new PointF(1.5f, 2.54f), new PointF(0.691f, 1.951f), new PointF(1, 1) };
//Draw Pentagon in page
diagram.Pages[0].DrawPolyline(1, 1, 2, 2, ps);

// Save diagram
diagram.Save(dataDir + "DrawPentagonInPage_out.html", new HTMLSaveOptions());

{{< /highlight >}}

