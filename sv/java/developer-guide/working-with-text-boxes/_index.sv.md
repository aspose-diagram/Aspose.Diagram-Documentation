---
title: Arbeta med textrutor
type: docs
weight: 200
url: /sv/java/working-with-text-boxes/
---
## **Formatera text i Visio Shapes textblocksektion**
 Aspose.Diagram API låter utvecklare styra textriktningen, justeringen, marginalerna, bakgrundsfärgen, bakgrundsfärgens transparens och standardtabbstopppositionen för text i en forms textblock. De kan interagera med dessa egenskaper programmatiskt med hjälp av[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).
### **Ställ in riktning, justering, marginaler, bakgrundsfärg, transparens och standardtabbstoppposition för texten i en forms textblock**
 Textblockformatsektionen i formarket Visio innehåller formateringsinformationen. De[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) klasserbjudanden[Textblock](https://reference.aspose.com/diagram/java/com.aspose.diagram/TextBlock) egenskap för att få eller ställa in det visuella utseendet på formens text.
### **Formatera text Programmeringsexempel**
Följande kodbit anger riktning, justering, marginaler, bakgrundsfärg, bakgrundsfärgstransparens och standardtabbstoppposition för orienteringsvinkeln och positionen för formens text överst.


{{< highlight java >}}
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

## **Rotera och ställ in positionen för formtexten**
Aspose.Diagram API låter utvecklare justera textpositionen och även rotera text på Visio Shape. För att utföra denna uppgift tillhandahåller textomvandlingssektionen på formarket egenskaperna TxtPin, TxtLocPin, TxtWidth och TxtHeight. Utvecklare kan interagera med dessa egenskaper programmatiskt med Aspose.Diagram API.

Textomvandlingsavsnittet innehåller positionsinformation om en forms textblock. Dessa exempel visar hur du justerar formtextpositioner och orienteringsvinkel:

- [Ställ in formens textposition överst](/diagram/sv/java/working-with-text-boxes/).
- [Ställ in formens textposition längst ner](/diagram/sv/java/working-with-text-boxes/).
- [Ställ in formens textposition till vänster](/diagram/sv/java/working-with-text-boxes/).
- [Ställ in formens textposition till höger](/diagram/sv/java/working-with-text-boxes/).
### **Ställ in formens textposition överst**
Följande kodbit anger orienteringsvinkel och position för formens text överst.


{{< highlight java >}}
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

### **Ställ in formens textposition längst ner**
Följande kod anger orienteringsvinkel och position för formens text längst ner.


{{< highlight java >}}
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

### **Ställ in formens textposition till vänster**
Följande kodbit anger orienteringsvinkel och position för formens text till vänster.


{{< highlight java >}}
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

### **Ställ in formens textposition till höger**
Följande kodbit anger orienteringsvinkel och position för formens text till höger.


{{< highlight java >}}
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

