---
title: dibujar texto
type: docs
weight: 5
url: /es/net/drawing/draw-text
description: Esta sección explica cómo dibujar texto en una página visio con Aspose.Diagram. Admite el uso de C# para dibujar texto y guardarlo como pdf, svg, html, image, xps y otros formatos.
---
## **Dibujar texto en Visio**
Aspose.Diagram for .NET API permite a los desarrolladores dibujar una forma de texto en una página. El siguiente ejemplo de código muestra cómo dibujar un texto en un dibujo Visio.


{{< highlight csharp >}}
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


## **Dibujar texto en SVG**
Aspose.Diagram for .NET API allows developers to draw a text in the page and save as SVG format. The code example below shows how to draw a text in a Visio drawing and save as SVG format.


{{< highlight csharp >}}
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


## **Dibujar texto en PDF**
Aspose.Diagram for .NET API allows developers to draw a text in the page and save as PDF format. The code example below shows how to draw a text in a Visio drawing and save as PDF format.


{{< highlight csharp >}}
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


## **Dibujar texto en PNG**
Aspose.Diagram for .NET API allows developers to draw a text in the page and save as PNG format. The code example below shows how to draw a text in a Visio drawing and save as PNG format.


{{< highlight csharp >}}
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


## **Dibujar texto en HTML**
Aspose.Diagram for .NET API allows developers to draw a text in the page and save as HTML format. The code example below shows how to draw a text in a Visio drawing and save as HTML format.


{{< highlight csharp >}}
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

