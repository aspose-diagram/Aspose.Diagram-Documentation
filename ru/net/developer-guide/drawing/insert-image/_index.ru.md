---
title: Вставить изображение
type: docs
weight: 70
url: /ru/net/drawing/insert-image
description: В этом разделе объясняется, как вставить изображение на страницу visio с помощью Aspose.Diagram. Поддержка использования C# для вставки изображения и сохранения в форматах pdf, svg, html, image, xps и других форматах.
---
[Страница](http://www.aspose.com/api/net/diagram/aspose.diagram/page)объект представляет область рисования страницы переднего плана или страницы фона. Свойство Pages, предоставляемое[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) Класс поддерживает набор объектов Aspose.Diagram.Page.

## **Вставить изображение в Visio**
Aspose.Diagram for .NET API позволяет разработчикам вставлять фигуру изображения на страницу. В приведенном ниже примере кода показано, как вставить изображение в чертеж Visio.


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


## **Вставить изображение в SVG**
Aspose.Diagram for .NET API позволяет разработчикам вставлять фигуру изображения на страницу. В приведенном ниже примере кода показано, как вставить изображение в чертеж Visio и сохранить в формате SVG.


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


## **Вставить изображение в PNG**
Aspose.Diagram for .NET API позволяет разработчикам вставлять фигуру изображения на страницу. В приведенном ниже примере кода показано, как вставить изображение в чертеж Visio и сохранить в формате PNG.


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


## **Вставить изображение в PDF**
Aspose.Diagram for .NET API позволяет разработчикам вставлять фигуру изображения на страницу. В приведенном ниже примере кода показано, как вставить изображение в чертеж Visio и сохранить в формате PDF.


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


## **Вставить изображение в HTML**
Aspose.Diagram for .NET API позволяет разработчикам вставлять фигуру изображения на страницу. В приведенном ниже примере кода показано, как вставить изображение в чертеж Visio и сохранить в формате HTML.


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

