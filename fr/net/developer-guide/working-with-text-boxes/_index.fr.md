---
title: Travailler avec des zones de texte
type: docs
weight: 210
url: /fr/net/working-with-text-boxes/
description: Cette section explique comment formater une forme de texte avec Aspose.Diagram.
---
## **Mettre en forme le texte dans la section Bloc de texte de la forme Visio**
 Aspose.Diagram API permet aux développeurs de contrôler la direction du texte, l'alignement, les marges, la couleur d'arrière-plan, la transparence de la couleur d'arrière-plan et la position d'arrêt de tabulation par défaut du texte dans le bloc de texte d'une forme. Ils peuvent interagir avec ces propriétés par programmation en utilisant[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **Définir la direction, l'alignement, les marges, la couleur d'arrière-plan, la transparence et la position de taquet de tabulation par défaut du texte dans le bloc de texte d'une forme**
 La section de format de bloc de texte de la feuille de forme Visio contient les informations de formatage. La[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) offres de cours[Bloc de texte](http://www.aspose.com/api/net/diagram/aspose.diagram/textblock) propriété pour obtenir ou définir l'apparence visuelle du texte de la forme.
### **Exemple de programmation de format de texte**
Le morceau de code suivant définit la direction, l'alignement, les marges, la couleur d'arrière-plan, la transparence de la couleur d'arrière-plan et la position de taquet de tabulation par défaut de l'angle d'orientation et la position du texte de la forme en haut.


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

## **Faire pivoter et définir la position du texte de forme Visio**
 Aspose.Diagram API permet aux développeurs d'ajuster la position du texte et également de faire pivoter le texte sur la forme Visio. Pour accomplir cette tâche, la section des transformations de texte sur la feuille de formes fournit les propriétés TxtPin, TxtLocPin, TxtWidth et TxtHeight. Les développeurs peuvent interagir avec ces propriétés par programmation en utilisant[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **Faire pivoter et définir la position du texte de la forme**
La section des transformations de texte contient les informations de position sur le bloc de texte d'une forme. Les exemples ci-dessous montrent comment ajuster les positions du texte de forme et l'angle d'orientation.
#### **Définir la position du texte de la forme en haut**
Le morceau de code suivant définit l'angle d'orientation et la position du texte de la forme en haut.


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

#### **Définir la position du texte de la forme en bas**
Le morceau de code suivant définit l'angle d'orientation et la position du texte de la forme en bas.


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

#### **Définir la position du texte de la forme à gauche**
Le morceau de code suivant définit l'angle d'orientation et la position du texte de la forme à gauche.


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

#### **Définir la position du texte de la forme à droite**
Le morceau de code suivant définit l'angle d'orientation et la position du texte de la forme à droite.


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

