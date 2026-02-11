---
title: إدراج صورة
type: docs
weight: 70
url: /ar/net/drawing/insert-image
description: يشرح هذا القسم كيفية إدراج صورة في صفحة visio مع Aspose.Diagram. الدعم باستخدام C# لإدراج الصورة وحفظها بتنسيق pdf و svg و html و image و xps وتنسيقات أخرى.
---
 ال[صفحة](http://www.aspose.com/api/net/diagram/aspose.diagram/page)يمثل الكائن منطقة الرسم لصفحة أمامية أو صفحة خلفية. خاصية الصفحات التي يعرضها ملف[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) فئة تدعم مجموعة من Aspose.Diagram.Page كائنات.

## **أدخل الصورة في Visio**
Aspose.Diagram for .NET API يسمح للمطورين بإدخال شكل صورة في الصفحة. يوضح مثال الكود أدناه كيفية إدراج صورة في رسم Visio.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
Page page = diagram.Pages[0];       
double pinX = 3, pinY = 3, width = 4, hieght = 4;
using (FileStream fs = new FileStream("image.png", FileMode.Open))
{
    page.AddShape(pinX, pinY, width, hieght, fs);
}
// Save diagram
diagram.Save(dataDir + "AddImageToPage_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


## **أدخل الصورة في SVG**
Aspose.Diagram for .NET API يسمح للمطورين بإدخال شكل صورة في الصفحة. يوضح مثال الكود أدناه كيفية إدراج صورة في رسم Visio وحفظها بتنسيق SVG.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
Page page = diagram.Pages[0];       
double pinX = 3, pinY = 3, width = 4, hieght = 4;
using (FileStream fs = new FileStream("image.png", FileMode.Open))
{
    page.AddShape(pinX, pinY, width, hieght, fs);
}
// Save diagram
diagram.Save(dataDir + "AddImageToPage_out.svg", SaveFileFormat.SVG);

{{< /highlight >}}


## **أدخل الصورة في PNG**
Aspose.Diagram for .NET API يسمح للمطورين بإدخال شكل صورة في الصفحة. يوضح مثال الكود أدناه كيفية إدراج صورة في رسم Visio وحفظها بتنسيق PNG.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
Page page = diagram.Pages[0];       
double pinX = 3, pinY = 3, width = 4, hieght = 4;
using (FileStream fs = new FileStream("image.png", FileMode.Open))
{
    page.AddShape(pinX, pinY, width, hieght, fs);
}
// Save diagram
diagram.Save(dataDir + "AddImageToPage_out.png", SaveFileFormat.PNG);

{{< /highlight >}}


## **أدخل الصورة في PDF**
Aspose.Diagram for .NET API يسمح للمطورين بإدخال شكل صورة في الصفحة. يوضح مثال الكود أدناه كيفية إدراج صورة في رسم Visio وحفظها بتنسيق PDF.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
Page page = diagram.Pages[0];       
double pinX = 3, pinY = 3, width = 4, hieght = 4;
using (FileStream fs = new FileStream("image.png", FileMode.Open))
{
    page.AddShape(pinX, pinY, width, hieght, fs);
}
// Save diagram
diagram.Save(dataDir + "AddImageToPage_out.pdf", SaveFileFormat.PDF);

{{< /highlight >}}


## **أدخل الصورة في HTML**
Aspose.Diagram for .NET API يسمح للمطورين بإدخال شكل صورة في الصفحة. يوضح مثال الكود أدناه كيفية إدراج صورة في رسم Visio وحفظها بتنسيق HTML.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
Page page = diagram.Pages[0];       
double pinX = 3, pinY = 3, width = 4, hieght = 4;
using (FileStream fs = new FileStream("image.png", FileMode.Open))
{
    page.AddShape(pinX, pinY, width, hieght, fs);
}
// Save diagram
diagram.Save(dataDir + "AddImageToPage_out.html", new HTMLSaveOptions());

{{< /highlight >}}

