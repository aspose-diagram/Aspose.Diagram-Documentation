---
title: Working with Text Boxes
type: docs
weight: 200
url: /java/working-with-text-boxes/
---

## **Format Text in the Visio Shape's Text Block Section**
Aspose.Diagram API allows developers to control the text direction, alignment, margins, background color, background color transparency, and default tab stop position of text in a shape's text block. They can interact with these properties programmatically using [Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).
### **Set the direction, alignment, margins, background color, transparency, and default tab stop position of the text in a Shape's Text Block**
The text block format section of the Visio shape sheet contains the formatting information. The [Shape](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) class offers [TextBlock](https://reference.aspose.com/diagram/java/com.aspose.diagram/TextBlock) property to get or set the visual appearance of the shape's text.
### **Format Text Programming Sample**
The following piece of code sets direction, alignment, margins, background color, background color transparency, and default tab stop position of the orientation angle and position of the shape's text at the top.

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
## **Rotate and Set Position of the Shape Text**
Aspose.Diagram API allows developers to adjust the text position and also rotate text on the Visio Shape. To accomplish this task, the text transforms section on the shapesheet provides TxtPin, TxtLocPin, TxtWidth and TxtHeight properties. Developers can interact with these properties programmatically using Aspose.Diagram API.

The text transforms section contains the positional information about a shape's text block. These examples show how to adjust shape text positions and orientation angle:

- [Set shape's text position at the top](/diagram/java/working-with-text-boxes/).
- [Set shape's text position at the bottom](/diagram/java/working-with-text-boxes/).
- [Set shape's text position at the left](/diagram/java/working-with-text-boxes/).
- [Set shape's text position at the right](/diagram/java/working-with-text-boxes/).
### **Set shape's text position at the top**
The following piece of code sets orientation angle and position of the shape's text at the top.

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
### **Set shape's text position at the bottom**
The following piece of code sets orientation angle and position of the shape's text at the bottom.

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
### **Set shape's text position at the left**
The following piece of code sets orientation angle and position of the shape's text at the left.

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
### **Set shape's text position at the right**
The following piece of code sets orientation angle and position of the shape's text at the right.

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
