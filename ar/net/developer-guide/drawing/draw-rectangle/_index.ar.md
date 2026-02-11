---
title: ارسم مستطيل
type: docs
weight: 10
url: /ar/net/drawing/draw-rectangle
description: يشرح هذا القسم كيفية رسم مستطيل في صفحة visio باستخدام Aspose.Diagram. الدعم باستخدام C# لرسم مستطيل وحفظه بتنسيق pdf و svg و html و image و xps وتنسيقات أخرى.
---
## **ارسم مستطيلاً في Visio**
Aspose.Diagram for .NET API يسمح للمطورين برسم شكل مستطيل في الصفحة. يوضح مثال الكود أدناه كيفية رسم مستطيل في رسم Visio.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Draw Rectangle in page
diagram.Pages[0].DrawRectangle(1, 2, 2, 4);

// Save diagram
diagram.Save(dataDir + "DrawRectangleInPage_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


## **ارسم مستطيلاً في SVG**
Aspose.Diagram for .NET API يسمح للمطورين برسم مستطيل في الصفحة وحفظه بتنسيق SVG. يوضح مثال الكود أدناه كيفية رسم مستطيل في رسم Visio وحفظه بتنسيق SVG.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Draw Rectangle in page
diagram.Pages[0].DrawRectangle(1, 2, 2, 4);

// Save diagram as SVG images
SVGSaveOptions imageSaveOptions = new SVGSaveOptions();
imageSaveOptions.PageIndex = 0;
diagram.Save(dataDir + "DrawRectangleInPage_out.svg", imageSaveOptions);

{{< /highlight >}}


## **ارسم مستطيلاً في PDF**
Aspose.Diagram for .NET API يسمح للمطورين برسم مستطيل في الصفحة وحفظه بتنسيق PDF. يوضح مثال الكود أدناه كيفية رسم مستطيل في رسم Visio وحفظه بتنسيق PDF.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Draw Rectangle in page
diagram.Pages[0].DrawRectangle(1, 2, 2, 4);

// Save diagram
diagram.Save(dataDir + "DrawRectangleInPage_out.pdf", new PdfSaveOptions());

{{< /highlight >}}


## **ارسم مستطيلاً في PNG**
Aspose.Diagram for .NET API يسمح للمطورين برسم مستطيل في الصفحة وحفظه بتنسيق PNG. يوضح مثال الكود أدناه كيفية رسم مستطيل في رسم Visio وحفظه بتنسيق PNG.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Draw Rectangle in page
diagram.Pages[0].DrawRectangle(1, 2, 2, 4);

// Save diagram as PNG image
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFileFormat.PNG);
imageSaveOptions.PageIndex = 0;
diagram.Save(dataDir + "DrawRectangleInPage_out.png", imageSaveOptions);

{{< /highlight >}}


## **ارسم مستطيلاً في HTML**
Aspose.Diagram for .NET API يسمح للمطورين برسم مستطيل في الصفحة وحفظه بتنسيق HTML. يوضح مثال الكود أدناه كيفية رسم مستطيل في رسم Visio وحفظه بتنسيق HTML.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Draw Rectangle in page
diagram.Pages[0].DrawRectangle(1, 2, 2, 4);

// Save diagram
diagram.Save(dataDir + "DrawRectangleInPage_out.html", new HTMLSaveOptions());

{{< /highlight >}}

