---
title: Lavorare con le caselle di testo
type: docs
weight: 210
url: /it/net/working-with-text-boxes/
description: Questa sezione spiega come formattare una forma di testo con Aspose.Diagram.
---
## **Formattare il testo nella sezione del blocco di testo della forma Visio**
 Aspose.Diagram API consente agli sviluppatori di controllare la direzione del testo, l'allineamento, i margini, il colore di sfondo, la trasparenza del colore di sfondo e la posizione di tabulazione predefinita del testo nel blocco di testo di una forma. Possono interagire con queste proprietà a livello di codice utilizzando[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **Imposta la direzione, l'allineamento, i margini, il colore di sfondo, la trasparenza e la posizione di tabulazione predefinita del testo nel Blocco di testo di una forma**
 La sezione del formato del blocco di testo dello shapesheet Visio contiene le informazioni sulla formattazione. Il[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) offerte di classe[Blocco di testo](http://www.aspose.com/api/net/diagram/aspose.diagram/textblock) property per ottenere o impostare l'aspetto visivo del testo della forma.
### **Esempio di programmazione del testo in formato**
La parte di codice seguente imposta la direzione, l'allineamento, i margini, il colore di sfondo, la trasparenza del colore di sfondo e la posizione di tabulazione predefinita dell'angolo di orientamento e la posizione del testo della forma nella parte superiore.


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

## **Ruota e imposta la posizione del testo forma Visio**
 Aspose.Diagram API consente agli sviluppatori di regolare la posizione del testo e anche di ruotare il testo sulla forma Visio. Per eseguire questa attività, la sezione di trasformazione del testo nel foglio di forma fornisce le proprietà TxtPin, TxtLocPin, TxtWidth e TxtHeight. Gli sviluppatori possono interagire con queste proprietà a livello di codice utilizzando[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **Ruota e imposta la posizione del testo della forma**
La sezione delle trasformazioni del testo contiene le informazioni sulla posizione del blocco di testo di una forma. Gli esempi seguenti mostrano come regolare le posizioni del testo della forma e l'angolo di orientamento.
#### **Imposta la posizione del testo della forma in alto**
La parte di codice seguente imposta l'angolo di orientamento e la posizione del testo della forma in alto.


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

#### **Imposta la posizione del testo della forma in basso**
La parte di codice seguente imposta l'angolo di orientamento e la posizione del testo della forma in basso.


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

#### **Imposta la posizione del testo della forma a sinistra**
La parte di codice seguente imposta l'angolo di orientamento e la posizione del testo della forma a sinistra.


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

#### **Imposta la posizione del testo della forma a destra**
La parte di codice seguente imposta l'angolo di orientamento e la posizione del testo della forma a destra.


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

