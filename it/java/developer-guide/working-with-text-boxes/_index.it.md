---
title: Lavorare con le caselle di testo
type: docs
weight: 200
url: /it/java/working-with-text-boxes/
---
## **Formattare il testo nella sezione del blocco di testo della forma Visio**
 Aspose.Diagram API consente agli sviluppatori di controllare la direzione del testo, l'allineamento, i margini, il colore di sfondo, la trasparenza del colore di sfondo e la posizione di tabulazione predefinita del testo nel blocco di testo di una forma. Possono interagire con queste proprietà a livello di codice utilizzando[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).
### **Imposta la direzione, l'allineamento, i margini, il colore di sfondo, la trasparenza e la posizione di tabulazione predefinita del testo nel Blocco di testo di una forma**
 La sezione del formato del blocco di testo del foglio di forma Visio contiene le informazioni sulla formattazione. Il[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) offerte di classe[Blocco di testo](https://reference.aspose.com/diagram/java/com.aspose.diagram/TextBlock) property per ottenere o impostare l'aspetto visivo del testo della forma.
### **Esempio di programmazione del testo in formato**
La parte di codice seguente imposta la direzione, l'allineamento, i margini, il colore di sfondo, la trasparenza del colore di sfondo e la posizione di tabulazione predefinita dell'angolo di orientamento e la posizione del testo della forma nella parte superiore.

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
## **Ruota e imposta la posizione del testo della forma**
Aspose.Diagram API consente agli sviluppatori di regolare la posizione del testo e anche di ruotare il testo sulla forma Visio. Per eseguire questa attività, la sezione di trasformazione del testo nel foglio di forma fornisce le proprietà TxtPin, TxtLocPin, TxtWidth e TxtHeight. Gli sviluppatori possono interagire con queste proprietà a livello di codice usando Aspose.Diagram API.

La sezione delle trasformazioni del testo contiene le informazioni sulla posizione del blocco di testo di una forma. Questi esempi mostrano come regolare le posizioni del testo della forma e l'angolo di orientamento:

- [Imposta la posizione del testo della forma in alto](/diagram/it/java/working-with-text-boxes/).
- [Imposta la posizione del testo della forma in basso](/diagram/it/java/working-with-text-boxes/).
- [Imposta la posizione del testo della forma a sinistra](/diagram/it/java/working-with-text-boxes/).
- [Imposta la posizione del testo della forma a destra](/diagram/it/java/working-with-text-boxes/).
### **Imposta la posizione del testo della forma in alto**
La parte di codice seguente imposta l'angolo di orientamento e la posizione del testo della forma in alto.

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
### **Imposta la posizione del testo della forma in basso**
La parte di codice seguente imposta l'angolo di orientamento e la posizione del testo della forma in basso.

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
### **Imposta la posizione del testo della forma a sinistra**
La parte di codice seguente imposta l'angolo di orientamento e la posizione del testo della forma a sinistra.

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
### **Imposta la posizione del testo della forma a destra**
La parte di codice seguente imposta l'angolo di orientamento e la posizione del testo della forma a destra.

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
