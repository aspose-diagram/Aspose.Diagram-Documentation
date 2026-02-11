---
title: ارسم قطع ناقص
type: docs
weight: 20
url: /ar/net/drawing/draw-ellipse
description: يشرح هذا القسم كيفية رسم شكل بيضاوي أو دائرة أو بيضاوي في صفحة visio باستخدام Aspose.Diagram. دعم باستخدام C# لرسم دائرة أو بيضاوي وحفظها بتنسيق pdf و svg و html و image و xps وتنسيقات أخرى.
---
## **ارسم دائرة في Visio**
Aspose.Diagram for .NET API يسمح للمطورين برسم شكل دائرة في الصفحة. يوضح مثال الكود أدناه كيفية رسم دائرة في رسم Visio.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
//Draw ellipse in diagram
diagram.Pages[0].DrawEllipse(1, 1, 2, 2);
// Save diagram
diagram.Save(dataDir + "DrawEllipseInPage_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```

## **ارسم دائرة في SVG**
Aspose.Diagram for .NET API يسمح للمطورين برسم دائرة في الصفحة وحفظها بتنسيق SVG. يوضح مثال الكود أدناه كيفية رسم دائرة في رسم Visio وحفظها بتنسيق SVG.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
//Draw ellipse in diagram
diagram.Pages[0].DrawEllipse(1, 1, 2, 2);
// Save diagram as SVG images
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFileFormat.SVG);
imageSaveOptions.PageIndex = 0;
diagram.Save(dataDir + "DrawEllipseInPage_out.svg", imageSaveOptions);

{{< /highlight >}}
```

## **ارسم دائرة في PDF**
Aspose.Diagram for .NET API يسمح للمطورين برسم دائرة في الصفحة وحفظها بتنسيق PDF. يوضح مثال الكود أدناه كيفية رسم دائرة في رسم Visio وحفظها بتنسيق PDF.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
//Draw ellipse in diagram
diagram.Pages[0].DrawEllipse(1, 1, 2, 2);
// Save diagram
diagram.Save(dataDir + "DrawEllipseInPage_out.pdf", new PdfSaveOptions());

{{< /highlight >}}
```

## **ارسم دائرة في PNG**
Aspose.Diagram for .NET API يسمح للمطورين برسم دائرة في الصفحة وحفظها بتنسيق PNG. يوضح مثال الكود أدناه كيفية رسم دائرة في رسم Visio وحفظها بتنسيق PNG.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
//Draw ellipse in diagram
diagram.Pages[0].DrawEllipse(1, 1, 2, 2);
// Save diagram as PNG image
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFileFormat.PNG);
imageSaveOptions.PageIndex = 0;
diagram.Save(dataDir + "DrawEllipseInPage_out.png", imageSaveOptions);

{{< /highlight >}}
```

## **ارسم دائرة في HTML**
Aspose.Diagram for .NET API يسمح للمطورين برسم دائرة في الصفحة وحفظها بتنسيق HTML. يوضح مثال الكود أدناه كيفية رسم دائرة في رسم Visio وحفظها بتنسيق HTML.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
//Draw ellipse in diagram
diagram.Pages[0].DrawEllipse(1, 1, 2, 2);
// Save diagram
diagram.Save(dataDir + "DrawEllipseInPage_out.html", new HTMLSaveOptions());

{{< /highlight >}}
```

## **ارسم شكل بيضوي في Visio**
Aspose.Diagram for .NET API يسمح للمطورين برسم شكل بيضاوي في الصفحة. يوضح مثال الكود أدناه كيفية رسم شكل بيضاوي في رسم Visio.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
//Draw ellipse in diagram
diagram.Pages[0].DrawEllipse(1, 2, 2, 4);
// Save diagram
diagram.Save(dataDir + "DrawEllipseInPage_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```

## **ارسم شكل بيضوي في SVG**
Aspose.Diagram for .NET API يسمح للمطورين برسم شكل بيضاوي في الصفحة وحفظه بتنسيق SVG. يوضح مثال الكود أدناه كيفية رسم شكل بيضاوي في رسم Visio وحفظه بتنسيق SVG.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
//Draw ellipse in diagram
diagram.Pages[0].DrawEllipse(1, 2, 2, 4);
// Save diagram as SVG images
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFileFormat.SVG);
imageSaveOptions.PageIndex = 0;
diagram.Save(dataDir + "DrawEllipseInPage_out.svg", imageSaveOptions);

{{< /highlight >}}
```

## **ارسم شكل بيضوي في PDF**
Aspose.Diagram for .NET API يسمح للمطورين برسم شكل بيضاوي في الصفحة وحفظه بتنسيق PDF. يوضح مثال الكود أدناه كيفية رسم شكل بيضاوي في رسم Visio وحفظه بتنسيق PDF.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
//Draw ellipse in diagram
diagram.Pages[0].DrawEllipse(1, 2, 2, 4);
// Save diagram
diagram.Save(dataDir + "DrawEllipseInPage_out.pdf", new PdfSaveOptions());

{{< /highlight >}}
```

## **ارسم شكل بيضوي في PNG**
Aspose.Diagram for .NET API يسمح للمطورين برسم شكل بيضاوي في الصفحة وحفظه بتنسيق PNG. يوضح مثال الكود أدناه كيفية رسم شكل بيضاوي في رسم Visio وحفظه بتنسيق PNG.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
//Draw ellipse in diagram
diagram.Pages[0].DrawEllipse(1, 2, 2, 4);
// Save diagram as PNG image
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFileFormat.PNG);
imageSaveOptions.PageIndex = 0;
diagram.Save(dataDir + "DrawEllipseInPage_out.png", imageSaveOptions);

{{< /highlight >}}
```

## **ارسم شكل بيضوي في HTML**
Aspose.Diagram for .NET API يسمح للمطورين برسم شكل بيضاوي في الصفحة وحفظه بتنسيق HTML. يوضح مثال الكود أدناه كيفية رسم شكل بيضاوي في رسم Visio وحفظه بتنسيق HTML.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Draw ellipse in diagram
diagram.Pages[0].DrawEllipse(1, 2, 2, 4);
// Save diagram
diagram.Save(dataDir + "DrawEllipseInPage_out.html", new HTMLSaveOptions());

{{< /highlight >}}
```

