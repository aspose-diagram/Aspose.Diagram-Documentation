---
title: Trabajar con cuadros de texto
type: docs
weight: 200
url: /es/java/working-with-text-boxes/
---
## **Dar formato al texto en la sección de bloque de texto de la forma Visio**
 Aspose.Diagram API permite a los desarrolladores controlar la dirección del texto, la alineación, los márgenes, el color de fondo, la transparencia del color de fondo y la posición de tabulación predeterminada del texto en el bloque de texto de una forma. Pueden interactuar con estas propiedades programáticamente usando[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).
### **Establecer la dirección, la alineación, los márgenes, el color de fondo, la transparencia y la posición de tabulación predeterminada del texto en el bloque de texto de una forma**
 La sección de formato de bloque de texto de la hoja de forma Visio contiene la información de formato. los[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) ofertas de clases[Bloque de texto](https://reference.aspose.com/diagram/java/com.aspose.diagram/TextBlock) propiedad para obtener o establecer la apariencia visual del texto de la forma.
### **Ejemplo de programación de formato de texto**
El siguiente fragmento de código establece la dirección, la alineación, los márgenes, el color de fondo, la transparencia del color de fondo y la posición de tabulación predeterminada del ángulo de orientación y la posición del texto de la forma en la parte superior.

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
## **Girar y establecer la posición del texto de forma**
Aspose.Diagram API permite a los desarrolladores ajustar la posición del texto y también girar el texto en la Forma Visio. Para realizar esta tarea, la sección de transformación de texto en la hoja de formas proporciona las propiedades TxtPin, TxtLocPin, TxtWidth y TxtHeight. Los desarrolladores pueden interactuar con estas propiedades mediante programación usando Aspose.Diagram API.

La sección de transformación de texto contiene la información posicional sobre el bloque de texto de una forma. Estos ejemplos muestran cómo ajustar las posiciones del texto de forma y el ángulo de orientación:

- [Establecer la posición del texto de la forma en la parte superior](/diagram/es/java/working-with-text-boxes/).
- [Establecer la posición del texto de la forma en la parte inferior](/diagram/es/java/working-with-text-boxes/).
- [Establecer la posición del texto de la forma a la izquierda](/diagram/es/java/working-with-text-boxes/).
- [Establecer la posición del texto de la forma a la derecha](/diagram/es/java/working-with-text-boxes/).
### **Establecer la posición del texto de la forma en la parte superior**
El siguiente fragmento de código establece el ángulo de orientación y la posición del texto de la forma en la parte superior.

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
### **Establecer la posición del texto de la forma en la parte inferior**
El siguiente fragmento de código establece el ángulo de orientación y la posición del texto de la forma en la parte inferior.

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
### **Establecer la posición del texto de la forma a la izquierda**
El siguiente fragmento de código establece el ángulo de orientación y la posición del texto de la forma a la izquierda.

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
### **Establecer la posición del texto de la forma a la derecha**
El siguiente fragmento de código establece el ángulo de orientación y la posición del texto de la forma a la derecha.

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
