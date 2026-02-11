---
title: Arbeta med textrutor
type: docs
weight: 210
url: /sv/net/working-with-text-boxes/
description: Det här avsnittet förklarar hur man formaterar en textform med Aspose.Diagram.
---
## **Formatera text i Visio Shapes textblocksektion**
 Aspose.Diagram API låter utvecklare styra textriktningen, justeringen, marginalerna, bakgrundsfärgen, bakgrundsfärgens transparens och standardtabbstopppositionen för text i en forms textblock. De kan interagera med dessa egenskaper programmatiskt med hjälp av[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **Ställ in riktning, justering, marginaler, bakgrundsfärg, transparens och standardtabbstoppposition för texten i en forms textblock**
 Textblockformatsektionen i formarket Visio innehåller formateringsinformationen. De[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) klasserbjudanden[Textblock](http://www.aspose.com/api/net/diagram/aspose.diagram/textblock) egenskap för att få eller ställa in det visuella utseendet på formens text.
### **Formatera text Programmeringsexempel**
Följande kodbit anger riktning, justering, marginaler, bakgrundsfärg, bakgrundsfärgstransparens och standardtabbstoppposition för orienteringsvinkeln och positionen för formens text överst.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeTextBoxData();
            
// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get the page by its name
Aspose.Diagram.Page page1 = diagram.Pages.GetPage("Page-1");
// Get shape by its ID
Aspose.Diagram.Shape shape = page1.Shapes.GetShape(1);
// Set orientation angle
DoubleValue margin = new DoubleValue(4, MeasureConst.PT);

// Set left, right, top and bottom margins of the shape's text block
shape.TextBlock.LeftMargin = margin;
shape.TextBlock.RightMargin = margin;
shape.TextBlock.TopMargin = margin;
shape.TextBlock.BottomMargin = margin;
// Set the text direction
shape.TextBlock.TextDirection.Value = TextDirectionValue.Vertical;
// Set the text alignment
shape.TextBlock.VerticalAlign.Value = VerticalAlignValue.Middle;
// Set the text block background color
shape.TextBlock.TextBkgnd.Ufe.F = "RGB(95,108,53)";
// Set the background color transparency in percent
shape.TextBlock.TextBkgndTrans.Value = 50;
// Set the distance between default tab stops for the selected shape.
shape.TextBlock.DefaultTabStop.Value = 2;

// Save Visio
diagram.Save(dataDir + "FormatShapeTextBlockSection_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Rotera och ställ in positionen för Visio-formtexten**
 Aspose.Diagram API låter utvecklare justera textpositionen och även rotera text på Visio Shape. För att utföra denna uppgift tillhandahåller textomvandlingssektionen på formarket egenskaperna TxtPin, TxtLocPin, TxtWidth och TxtHeight. Utvecklare kan interagera med dessa egenskaper programmatiskt med hjälp av[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **Rotera och ställ in positionen för formtexten**
Textomvandlingsavsnittet innehåller positionsinformation om en forms textblock. Nedan exempel visar hur man justerar formtextpositioner och orienteringsvinkel.
#### **Ställ in formens textposition överst**
Följande kodbit anger orienteringsvinkel och position för formens text överst.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeTextBoxData();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get shape
long shapeid = 1;
Shape shape = diagram.Pages.GetPage("Page-1").Shapes.GetShape(shapeid);

// Set text position at the top,
// TxtLocPinY = "TxtHeight*0" and TxtPinY = "Height*1"
shape.TextXForm.TxtLocPinY.Value = 0;
shape.TextXForm.TxtPinY.Value = shape.XForm.Height.Value;

// Set orientation angle
double angleDeg = 0;
double angleRad = (Math.PI / 180) * angleDeg;
shape.TextXForm.TxtAngle.Value = angleRad;

// Save Visio diagram in the local storage
diagram.Save(dataDir + "SetShapeTextPositionAtTop_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

#### **Ställ in formens textposition längst ner**
Följande kod anger orienteringsvinkel och position för formens text längst ner.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeTextBoxData();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get shape
long shapeid = 1;
Shape shape = diagram.Pages.GetPage("Page-1").Shapes.GetShape(shapeid);

// Set text position at the bottom,
// TxtLocPinY = "TxtHeight*1" and TxtPinY = "Height*0"
shape.TextXForm.TxtLocPinY.Value = shape.TextXForm.TxtHeight.Value;
shape.TextXForm.TxtPinY.Value = 0;

// Set orientation angle
double angleDeg = 0;
double angleRad = (Math.PI / 180) * angleDeg;
shape.TextXForm.TxtAngle.Value = angleRad;

// Save Visio diagram in the local storage
diagram.Save(dataDir + "SetShapeTextPositionAtBottom_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

#### **Ställ in formens textposition till vänster**
Följande kodbit anger orienteringsvinkel och position för formens text till vänster.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeTextBoxData();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get shape
long shapeid = 1;
Shape shape = diagram.Pages.GetPage("Page-1").Shapes.GetShape(shapeid);

// Set text position at the left,
// TxtLocPinX = "TxtWidth*1" and TxtPinX = "Width*0"
shape.TextXForm.TxtLocPinX.Value = shape.TextXForm.TxtWidth.Value;
shape.TextXForm.TxtPinX.Value = 0;
// Set orientation angle
double angleDeg = 0;
double angleRad = (Math.PI / 180) * angleDeg;
shape.TextXForm.TxtAngle.Value = angleRad;

// Save Visio diagram in the local storage
diagram.Save(dataDir + "SetShapeTextPositionAtLeft_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

#### **Ställ in formens textposition till höger**
Följande kodbit anger orienteringsvinkel och position för formens text till höger.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeTextBoxData();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get shape
long shapeid = 1;
Shape shape = diagram.Pages.GetPage("Page-1").Shapes.GetShape(shapeid);

// Set text position at the right,
// TxtLocPinX = "TxtWidth*0" and TxtPinX = "Width*1"
shape.TextXForm.TxtLocPinX.Value = 0;
shape.TextXForm.TxtPinX.Value = shape.XForm.Width.Value;
// Set orientation angle
double angleDeg = 0;
double angleRad = (Math.PI / 180) * angleDeg;
shape.TextXForm.TxtAngle.Value = angleRad;

// Save Visio diagram in the local storage
diagram.Save(dataDir + "SetShapeTextPositionAtRight_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

