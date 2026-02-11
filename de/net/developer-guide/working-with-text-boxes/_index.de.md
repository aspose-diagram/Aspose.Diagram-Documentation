---
title: Arbeiten mit Textfeldern
type: docs
weight: 210
url: /de/net/working-with-text-boxes/
description: In diesem Abschnitt wird erläutert, wie Sie eine Textform mit Aspose.Diagram formatieren.
---
## **Formatieren Sie Text im Textblockabschnitt der Form Visio**
 Aspose.Diagram API ermöglicht Entwicklern die Steuerung von Textrichtung, Ausrichtung, Rändern, Hintergrundfarbe, Hintergrundfarbentransparenz und Standard-Tabulatorposition von Text im Textblock einer Form. Sie können programmgesteuert mit diesen Eigenschaften interagieren[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **Legen Sie Richtung, Ausrichtung, Ränder, Hintergrundfarbe, Transparenz und Standard-Tabulatorposition des Textes im Textblock einer Form fest**
 Der Abschnitt Textblockformat des Shapesheets Visio enthält die Formatierungsinformationen. Das[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Klasse Angebote[Textblock](http://www.aspose.com/api/net/diagram/aspose.diagram/textblock) -Eigenschaft, um die visuelle Darstellung des Texts der Form abzurufen oder festzulegen.
### **Programmierbeispiel für Text formatieren**
Der folgende Codeabschnitt legt Richtung, Ausrichtung, Ränder, Hintergrundfarbe, Hintergrundfarbentransparenz und die Standard-Tabulatorposition des Ausrichtungswinkels und die Position des Texts der Form oben fest.

```
{{< highlight "csharp" >}}
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
```
## **Drehen und Position des Formtextes Visio festlegen**
 Mit Aspose.Diagram API können Entwickler die Textposition anpassen und auch Text auf der Visio-Form drehen. Um diese Aufgabe zu erfüllen, stellt der Texttransformationsabschnitt auf dem Shapesheet die Eigenschaften TxtPin, TxtLocPin, TxtWidth und TxtHeight bereit. Entwickler können programmgesteuert mit diesen Eigenschaften interagieren[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **Drehen und Position des Formtextes festlegen**
Der Abschnitt Texttransformationen enthält die Positionsinformationen zum Textblock einer Form. Die folgenden Beispiele zeigen, wie Sie die Position von Formtext und den Ausrichtungswinkel anpassen.
#### **Legen Sie die Textposition der Form oben fest**
Der folgende Codeabschnitt legt den Ausrichtungswinkel und die Position des Texts der Form oben fest.

```
{{< highlight "csharp" >}}
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
```
#### **Legen Sie die Textposition der Form unten fest**
Der folgende Codeabschnitt legt den Ausrichtungswinkel und die Position des Texts der Form unten fest.

```
{{< highlight "csharp" >}}
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
```
#### **Stellen Sie die Textposition der Form links ein**
Der folgende Codeabschnitt legt den Ausrichtungswinkel und die Position des Texts der Form auf der linken Seite fest.

```
{{< highlight "csharp" >}}
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
```
#### **Legen Sie die Textposition der Form rechts fest**
Der folgende Codeabschnitt legt den Ausrichtungswinkel und die Position des Texts der Form auf der rechten Seite fest.

```
{{< highlight "csharp" >}}
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
```
