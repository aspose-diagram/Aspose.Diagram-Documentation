---
title: Arbeiten mit Textfeldern
type: docs
weight: 200
url: /de/java/working-with-text-boxes/
---
## **Formatieren Sie Text im Textblockabschnitt der Form Visio**
 Aspose.Diagram API ermöglicht Entwicklern die Steuerung von Textrichtung, Ausrichtung, Rändern, Hintergrundfarbe, Hintergrundfarbentransparenz und Standard-Tabulatorposition von Text im Textblock einer Form. Sie können programmgesteuert mit diesen Eigenschaften interagieren[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).
### **Legen Sie Richtung, Ausrichtung, Ränder, Hintergrundfarbe, Transparenz und Standard-Tabulatorposition des Textes im Textblock einer Form fest**
 Der Abschnitt Textblockformat des Formblatts Visio enthält die Formatierungsinformationen. Das[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) Klasse Angebote[Textblock](https://reference.aspose.com/diagram/java/com.aspose.diagram/TextBlock) -Eigenschaft, um die visuelle Darstellung des Texts der Form abzurufen oder festzulegen.
### **Programmierbeispiel für Text formatieren**
Der folgende Codeabschnitt legt Richtung, Ausrichtung, Ränder, Hintergrundfarbe, Hintergrundfarbentransparenz und die Standard-Tabulatorposition des Ausrichtungswinkels und die Position des Texts der Form oben fest.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(FormatShapeTextBlockSection.class); 
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get the page by its name
Page page1 = diagram.getPages().getPage("Page-1");
// get shape by its ID
Shape shape = page1.getShapes().getShape(1);
// set orientation angle
DoubleValue margin = new DoubleValue(4, MeasureConst.PT);

// set left, right, top and bottom margins of the shape's text block
shape.getTextBlock().setLeftMargin(margin);
shape.getTextBlock().setRightMargin(margin);
shape.getTextBlock().setTopMargin(margin);
shape.getTextBlock().setBottomMargin(margin);

// set the text direction
shape.getTextBlock().getTextDirection().setValue(TextDirectionValue.VERTICAL);
// set the text alignment
shape.getTextBlock().getVerticalAlign().setValue(VerticalAlignValue.MIDDLE);
// set the text block background color
shape.getTextBlock().getTextBkgnd().getUfe().setF("RGB(95,108,53)");
// set the background color transparency in percent
shape.getTextBlock().getTextBkgndTrans().setValue(50);
// set the distance between default tab stops for the selected shape.
shape.getTextBlock().getDefaultTabStop().setValue(2);

// save Visio
diagram.save(dataDir + "FormatShapeTextBlockSection_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Drehen und Position des Formtextes festlegen**
Mit Aspose.Diagram API können Entwickler die Textposition anpassen und auch Text auf der Visio-Form drehen. Um diese Aufgabe zu erfüllen, stellt der Texttransformationsabschnitt auf dem Shapesheet die Eigenschaften TxtPin, TxtLocPin, TxtWidth und TxtHeight bereit. Entwickler können mit diesen Eigenschaften programmgesteuert interagieren, indem sie Aspose.Diagram API verwenden.

Der Abschnitt Texttransformationen enthält die Positionsinformationen zum Textblock einer Form. Diese Beispiele zeigen, wie Sie die Position von Formtext und den Ausrichtungswinkel anpassen:

- [Legen Sie die Textposition der Form oben fest](/diagram/de/java/working-with-text-boxes/).
- [Legen Sie die Textposition der Form unten fest](/diagram/de/java/working-with-text-boxes/).
- [Stellen Sie die Textposition der Form links ein](/diagram/de/java/working-with-text-boxes/).
- [Legen Sie die Textposition der Form rechts fest](/diagram/de/java/working-with-text-boxes/).
### **Legen Sie die Textposition der Form oben fest**
Der folgende Codeabschnitt legt den Ausrichtungswinkel und die Position des Texts der Form oben fest.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetShapeTextPositionAtTop.class);   
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get shape
long shapeid = 1;
Shape shape = diagram.getPages().getPage("Page-1").getShapes().getShape(shapeid);

	    // set text position at the top,
	    // TxtLocPinY = "TxtHeight*0" and TxtPinY = "Height*1"
	    shape.getTextXForm().getTxtLocPinY().setValue(0);
	    shape.getTextXForm().getTxtPinY().setValue(shape.getXForm().getHeight().getValue());
	
	    // set orientation angle
	    double angleDeg = 0;
	    double angleRad = (Math.PI / 180) * angleDeg;
	    shape.getTextXForm().getTxtAngle().setValue(angleRad);

// save Visio diagram in the local storage
diagram.save(dataDir + "SetShapeTextPositionAtTop_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
### **Legen Sie die Textposition der Form unten fest**
Der folgende Codeabschnitt legt den Ausrichtungswinkel und die Position des Texts der Form unten fest.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetShapeTextPositionAtBottom.class);  
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get shape
long shapeid = 1;
Shape shape = diagram.getPages().getPage("Page-1").getShapes().getShape(shapeid);

	     // set text position at the bottom,
	     // TxtLocPinY = "TxtHeight*1" and TxtPinY = "Height*0"
	     shape.getTextXForm().getTxtLocPinY().setValue(shape.getTextXForm().getTxtHeight().getValue());
	     shape.getTextXForm().getTxtPinY().setValue(0);
	
	     // set orientation angle
	     double angleDeg = 0;
	     double angleRad = (Math.PI / 180) * angleDeg;
	     shape.getTextXForm().getTxtAngle().setValue(angleRad);     

// save Visio diagram in the local storage
diagram.save(dataDir + "SetShapeTextPositionAtBottom_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
### **Stellen Sie die Textposition der Form links ein**
Der folgende Codeabschnitt legt den Ausrichtungswinkel und die Position des Texts der Form auf der linken Seite fest.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetShapeTextPositionAtLeft.class);  
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get shape
long shapeid = 1;
Shape shape = diagram.getPages().getPage("Page-1").getShapes().getShape(shapeid);

// set text position at the left,
// TxtLocPinX = "TxtWidth*1" and TxtPinX = "Width*0"
shape.getTextXForm().getTxtLocPinX().setValue(shape.getTextXForm().getTxtWidth().getValue());
shape.getTextXForm().getTxtPinX().setValue(0);
// set orientation angle
double angleDeg = 0;
double angleRad = (Math.PI / 180) * angleDeg;
shape.getTextXForm().getTxtAngle().setValue(angleRad);
        
// save Visio diagram in the local storage
diagram.save(dataDir + "SetShapeTextPositionAtLeft_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
### **Legen Sie die Textposition der Form rechts fest**
Der folgende Codeabschnitt legt den Ausrichtungswinkel und die Position des Texts der Form auf der rechten Seite fest.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetShapeTextPositionAtRight.class);  
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get shape
long shapeid = 1;
Shape shape = diagram.getPages().getPage("Page-1").getShapes().getShape(shapeid);

// set text position at the right,
// TxtLocPinX = "TxtWidth*0" and TxtPinX = "Width*1"
shape.getTextXForm().getTxtLocPinX().setValue(0);
shape.getTextXForm().getTxtPinX().setValue(shape.getXForm().getWidth().getValue());
// set orientation angle
double angleDeg = 0;
double angleRad = (Math.PI / 180) * angleDeg;
shape.getTextXForm().getTxtAngle().setValue(angleRad);
        
// save Visio diagram in the local storage
diagram.save(dataDir + "SetShapeTextPositionAtRight_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
