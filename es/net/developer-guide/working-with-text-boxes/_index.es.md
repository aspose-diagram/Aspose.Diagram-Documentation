---
title: Trabajar con cuadros de texto
type: docs
weight: 210
url: /es/net/working-with-text-boxes/
description: Esta sección explica cómo dar formato a una forma de texto con Aspose.Diagram.
---
## **Dar formato al texto en la sección de bloque de texto de la forma Visio**
 Aspose.Diagram API permite a los desarrolladores controlar la dirección del texto, la alineación, los márgenes, el color de fondo, la transparencia del color de fondo y la posición de tabulación predeterminada del texto en el bloque de texto de una forma. Pueden interactuar con estas propiedades programáticamente usando[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **Establecer la dirección, la alineación, los márgenes, el color de fondo, la transparencia y la posición de tabulación predeterminada del texto en el bloque de texto de una forma**
 La sección de formato de bloque de texto de la hoja de forma Visio contiene la información de formato. los[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) ofertas de clases[Bloque de texto](http://www.aspose.com/api/net/diagram/aspose.diagram/textblock) propiedad para obtener o establecer la apariencia visual del texto de la forma.
### **Ejemplo de programación de formato de texto**
El siguiente fragmento de código establece la dirección, la alineación, los márgenes, el color de fondo, la transparencia del color de fondo y la posición de tabulación predeterminada del ángulo de orientación y la posición del texto de la forma en la parte superior.

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
## **Girar y establecer la posición del texto de forma Visio**
 Aspose.Diagram API permite a los desarrolladores ajustar la posición del texto y también girar el texto en la Forma Visio. Para realizar esta tarea, la sección de transformación de texto en la hoja de formas proporciona las propiedades TxtPin, TxtLocPin, TxtWidth y TxtHeight. Los desarrolladores pueden interactuar con estas propiedades mediante programación mediante[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **Girar y establecer la posición del texto de forma**
La sección de transformación de texto contiene la información posicional sobre el bloque de texto de una forma. Los siguientes ejemplos muestran cómo ajustar las posiciones del texto de forma y el ángulo de orientación.
#### **Establecer la posición del texto de la forma en la parte superior**
El siguiente fragmento de código establece el ángulo de orientación y la posición del texto de la forma en la parte superior.

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
#### **Establecer la posición del texto de la forma en la parte inferior**
El siguiente fragmento de código establece el ángulo de orientación y la posición del texto de la forma en la parte inferior.

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
#### **Establecer la posición del texto de la forma a la izquierda**
El siguiente fragmento de código establece el ángulo de orientación y la posición del texto de la forma a la izquierda.

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
#### **Establecer la posición del texto de la forma a la derecha**
El siguiente fragmento de código establece el ángulo de orientación y la posición del texto de la forma a la derecha.

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
