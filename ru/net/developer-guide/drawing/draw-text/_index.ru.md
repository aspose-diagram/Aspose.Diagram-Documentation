---
title: Нарисовать текст
type: docs
weight: 5
url: /ru/net/drawing/draw-text
description: В этом разделе объясняется, как рисовать текст на странице visio с помощью Aspose.Diagram. Поддержка использования C# для рисования текста и сохранения в форматах pdf, svg, html, image, xps и других форматах.
---
## **Нарисовать текст в Visio**
Aspose.Diagram for .NET API позволяет разработчикам рисовать текст на странице. В приведенном ниже примере кода показано, как нарисовать текст на рисунке Visio.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Initiazlie a new PointF[]
PointF[] ps = new PointF[] { new PointF(1, 2), new PointF(2, 0), new PointF(3, 2), new PointF(2, 4), new PointF(1, 2) };
//Draw a diamond shape in page
long shapeId = diagram.Pages[0].DrawPolyline(2, 2, 4, 4, ps);
// get the added shape from page
Shape shape = diagram.Pages[0].Shapes.GetShape(shapeId);
// add text to shape
shape.Text.Value.Add(new Txt("Hello world!"));

//Aspose.Diagram.Char ch = new Aspose.Diagram.Char();
//shape.Chars.Add(ch);
//ch.IX = 0;
//// set text font
//ch.FontName.Value = "Courier New";
//// set text color
//ch.Color.Value = "#ff0000";
//// set font size, unit is 72pt
//ch.Size.Value = 16 / 72.0;

//Aspose.Diagram.Para para = new Para();
//shape.Paras.Add(para);
//para.IX = 0;
//// set horizon align
//para.HorzAlign.Value = HorzAlignValue.LeftAlign;
//// set indent
//para.IndLeft.Value = 1.2;

// Save diagram
diagram.Save(dataDir + "AddTextToShape_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```

## **Нарисовать текст в SVG**
Aspose.Diagram for .NET API позволяет разработчикам рисовать текст на странице и сохранять в формате SVG. В приведенном ниже примере кода показано, как нарисовать текст на чертеже Visio и сохранить его в формате SVG.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Initiazlie a new PointF[]
PointF[] ps = new PointF[] { new PointF(1, 2), new PointF(2, 0), new PointF(3, 2), new PointF(2, 4), new PointF(1, 2) };
//Draw a diamond shape in page
long shapeId = diagram.Pages[0].DrawPolyline(2, 2, 4, 4, ps);
// get the added shape from page
Shape shape = diagram.Pages[0].Shapes.GetShape(shapeId);
// add text to shape
shape.Text.Value.Add(new Txt("Hello world!"));

//Aspose.Diagram.Char ch = new Aspose.Diagram.Char();
//shape.Chars.Add(ch);
//ch.IX = 0;
//// set text font
//ch.FontName.Value = "Courier New";
//// set text color
//ch.Color.Value = "#ff0000";
//// set font size, unit is 72pt
//ch.Size.Value = 16 / 72.0;

//Aspose.Diagram.Para para = new Para();
//shape.Paras.Add(para);
//para.IX = 0;
//// set horizon align
//para.HorzAlign.Value = HorzAlignValue.LeftAlign;
//// set indent
//para.IndLeft.Value = 1.2;

// Save diagram as SVG images
SVGSaveOptions imageSaveOptions = new SVGSaveOptions();
imageSaveOptions.PageIndex = 0;
diagram.Save(dataDir + "AddTextToShape_out.svg", imageSaveOptions);

{{< /highlight >}}
```

## **Нарисовать текст в PDF**
Aspose.Diagram for .NET API позволяет разработчикам рисовать текст на странице и сохранять в формате PDF. В приведенном ниже примере кода показано, как нарисовать текст на чертеже Visio и сохранить его в формате PDF.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Initiazlie a new PointF[]
PointF[] ps = new PointF[] { new PointF(1, 2), new PointF(2, 0), new PointF(3, 2), new PointF(2, 4), new PointF(1, 2) };
//Draw a diamond shape in page
long shapeId = diagram.Pages[0].DrawPolyline(2, 2, 4, 4, ps);
// get the added shape from page
Shape shape = diagram.Pages[0].Shapes.GetShape(shapeId);
// add text to shape
shape.Text.Value.Add(new Txt("Hello world!"));

//Aspose.Diagram.Char ch = new Aspose.Diagram.Char();
//shape.Chars.Add(ch);
//ch.IX = 0;
//// set text font
//ch.FontName.Value = "Courier New";
//// set text color
//ch.Color.Value = "#ff0000";
//// set font size, unit is 72pt
//ch.Size.Value = 16 / 72.0;

//Aspose.Diagram.Para para = new Para();
//shape.Paras.Add(para);
//para.IX = 0;
//// set horizon align
//para.HorzAlign.Value = HorzAlignValue.LeftAlign;
//// set indent
//para.IndLeft.Value = 1.2;

// Save diagram
diagram.Save(dataDir + "AddTextToShape_out.pdf", new PdfSaveOptions());

{{< /highlight >}}
```

## **Нарисовать текст в PNG**
Aspose.Diagram for .NET API позволяет разработчикам рисовать текст на странице и сохранять в формате PNG. В приведенном ниже примере кода показано, как нарисовать текст на чертеже Visio и сохранить его в формате PNG.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Initiazlie a new PointF[]
PointF[] ps = new PointF[] { new PointF(1, 2), new PointF(2, 0), new PointF(3, 2), new PointF(2, 4), new PointF(1, 2) };
//Draw a diamond shape in page
long shapeId = diagram.Pages[0].DrawPolyline(2, 2, 4, 4, ps);
// get the added shape from page
Shape shape = diagram.Pages[0].Shapes.GetShape(shapeId);
// add text to shape
shape.Text.Value.Add(new Txt("Hello world!"));

//Aspose.Diagram.Char ch = new Aspose.Diagram.Char();
//shape.Chars.Add(ch);
//ch.IX = 0;
//// set text font
//ch.FontName.Value = "Courier New";
//// set text color
//ch.Color.Value = "#ff0000";
//// set font size, unit is 72pt
//ch.Size.Value = 16 / 72.0;

//Aspose.Diagram.Para para = new Para();
//shape.Paras.Add(para);
//para.IX = 0;
//// set horizon align
//para.HorzAlign.Value = HorzAlignValue.LeftAlign;
//// set indent
//para.IndLeft.Value = 1.2;

// Save diagram as PNG image
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFileFormat.PNG);
imageSaveOptions.PageIndex = 0;
diagram.Save(dataDir + "AddTextToShape_out.png", imageSaveOptions);

{{< /highlight >}}
```

## **Нарисовать текст в HTML**
Aspose.Diagram for .NET API позволяет разработчикам рисовать текст на странице и сохранять в формате HTML. В приведенном ниже примере кода показано, как нарисовать текст на чертеже Visio и сохранить его в формате HTML.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Initiazlie a new PointF[]
PointF[] ps = new PointF[] { new PointF(1, 2), new PointF(2, 0), new PointF(3, 2), new PointF(2, 4), new PointF(1, 2) };
//Draw a diamond shape in page
long shapeId = diagram.Pages[0].DrawPolyline(2, 2, 4, 4, ps);
// get the added shape from page
Shape shape = diagram.Pages[0].Shapes.GetShape(shapeId);
// add text to shape
shape.Text.Value.Add(new Txt("Hello world!"));

//Aspose.Diagram.Char ch = new Aspose.Diagram.Char();
//shape.Chars.Add(ch);
//ch.IX = 0;
//// set text font
//ch.FontName.Value = "Courier New";
//// set text color
//ch.Color.Value = "#ff0000";
//// set font size, unit is 72pt
//ch.Size.Value = 16 / 72.0;

//Aspose.Diagram.Para para = new Para();
//shape.Paras.Add(para);
//para.IX = 0;
//// set horizon align
//para.HorzAlign.Value = HorzAlignValue.LeftAlign;
//// set indent
//para.IndLeft.Value = 1.2;

// Save diagram
diagram.Save(dataDir + "AddTextToShape_out.html", new HTMLSaveOptions());

{{< /highlight >}}
```
