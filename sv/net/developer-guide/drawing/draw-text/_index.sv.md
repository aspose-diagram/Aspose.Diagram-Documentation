---
title: Rita text
type: docs
weight: 5
url: /sv/net/drawing/draw-text
description: Det här avsnittet förklarar hur man ritar text på en visio-sida med Aspose.Diagram. Stöd att använda C# för att rita text och spara som pdf, svg, html, bild, xps och andra format.
---
## **Rita text på Visio**
Aspose.Diagram for .NET API tillåter utvecklare att rita en textform på en sida. Kodexemplet nedan visar hur man ritar en text i en Visio-ritning.


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


## **Rita text på SVG**
Aspose.Diagram for .NET API låter utvecklare rita en text på sidan och spara i formatet SVG. Kodexemplet nedan visar hur man ritar en text i en Visio-ritning och sparar som SVG-format.


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


## **Rita text på PDF**
Aspose.Diagram for .NET API låter utvecklare rita en text på sidan och spara i formatet PDF. Kodexemplet nedan visar hur man ritar en text i en Visio-ritning och sparar som PDF-format.


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


## **Rita text på PNG**
Aspose.Diagram for .NET API låter utvecklare rita en text på sidan och spara i formatet PNG. Kodexemplet nedan visar hur man ritar en text i en Visio-ritning och sparar som PNG-format.


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


## **Rita text på HTML**
Aspose.Diagram for .NET API låter utvecklare rita en text på sidan och spara i formatet HTML. Kodexemplet nedan visar hur man ritar en text i en Visio-ritning och sparar som HTML-format.


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

