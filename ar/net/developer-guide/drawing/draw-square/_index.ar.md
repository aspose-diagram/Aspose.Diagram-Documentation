---
title: ارسم مربع
type: docs
weight: 50
url: /ar/net/drawing/draw-square
description: يشرح هذا القسم كيفية رسم مربع في صفحة visio باستخدام Aspose.Diagram. الدعم باستخدام C# لرسم مربع وحفظه بتنسيق pdf و svg و html و image و xps وتنسيقات أخرى.
---
## **ارسم مربعًا في Visio**
Aspose.Diagram for .NET API يسمح للمطورين برسم شكل مربع في الصفحة. يوضح مثال الكود أدناه كيفية رسم مربع في رسم Visio.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Draw square in page
diagram.Pages[0].DrawRectangle(1, 1, 2, 2);

// Save diagram
diagram.Save(dataDir + "DrawSquareInPage_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


## **ارسم مربعًا في SVG**
Aspose.Diagram for .NET API يسمح للمطورين برسم مربع في الصفحة وحفظه بتنسيق SVG. يوضح مثال الكود أدناه كيفية رسم مربع في رسم Visio وحفظه بتنسيق SVG.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Draw square in page
diagram.Pages[0].DrawRectangle(1, 1, 2, 2);

// Save diagram as SVG images
SVGSaveOptions imageSaveOptions = new SVGSaveOptions();
imageSaveOptions.PageIndex = 0;
diagram.Save(dataDir + "DrawSquareInPage_out.svg", imageSaveOptions);

{{< /highlight >}}


## **ارسم مربعًا في PDF**
Aspose.Diagram for .NET API يسمح للمطورين برسم مربع في الصفحة وحفظه بتنسيق PDF. يوضح مثال الكود أدناه كيفية رسم مربع في رسم Visio وحفظه بتنسيق PDF.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Draw square in page
diagram.Pages[0].DrawRectangle(1, 1, 2, 2);

// Save diagram
diagram.Save(dataDir + "DrawSquareInPage_out.pdf", new PdfSaveOptions());

{{< /highlight >}}


## **ارسم مربعًا في PNG**
Aspose.Diagram for .NET API يسمح للمطورين برسم مربع في الصفحة وحفظه بتنسيق PNG. يوضح مثال الكود أدناه كيفية رسم مربع في رسم Visio وحفظه بتنسيق PNG.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Draw square in page
diagram.Pages[0].DrawRectangle(1, 1, 2, 2);

// Save diagram as PNG image
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFileFormat.PNG);
imageSaveOptions.PageIndex = 0;
diagram.Save(dataDir + "DrawSquareInPage_out.png", imageSaveOptions);

{{< /highlight >}}


## **ارسم مربعًا في HTML**
Aspose.Diagram for .NET API يسمح للمطورين برسم مربع في الصفحة وحفظه بتنسيق HTML. يوضح مثال الكود أدناه كيفية رسم مربع في رسم Visio وحفظه بتنسيق HTML.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Draw square in page
diagram.Pages[0].DrawRectangle(1, 1, 2, 2);

// Save diagram
diagram.Save(dataDir + "DrawSquareInPage_out.html", new HTMLSaveOptions());

{{< /highlight >}}

