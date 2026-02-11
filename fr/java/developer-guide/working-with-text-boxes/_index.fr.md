---
title: Travailler avec des zones de texte
type: docs
weight: 200
url: /fr/java/working-with-text-boxes/
---
## **Mettre en forme le texte dans la section Bloc de texte de la forme Visio**
 Aspose.Diagram API permet aux développeurs de contrôler la direction du texte, l'alignement, les marges, la couleur d'arrière-plan, la transparence de la couleur d'arrière-plan et la position d'arrêt de tabulation par défaut du texte dans le bloc de texte d'une forme. Ils peuvent interagir avec ces propriétés par programmation en utilisant[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).
### **Définir la direction, l'alignement, les marges, la couleur d'arrière-plan, la transparence et la position de taquet de tabulation par défaut du texte dans le bloc de texte d'une forme**
 La section de format de bloc de texte de la feuille de forme Visio contient les informations de formatage. La[Forme](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) offres de cours[Bloc de texte](https://reference.aspose.com/diagram/java/com.aspose.diagram/TextBlock) propriété pour obtenir ou définir l'apparence visuelle du texte de la forme.
### **Exemple de programmation de format de texte**
Le morceau de code suivant définit la direction, l'alignement, les marges, la couleur d'arrière-plan, la transparence de la couleur d'arrière-plan et la position de taquet de tabulation par défaut de l'angle d'orientation et la position du texte de la forme en haut.

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
## **Faire pivoter et définir la position du texte de la forme**
Aspose.Diagram API permet aux développeurs d'ajuster la position du texte et également de faire pivoter le texte sur la forme Visio. Pour accomplir cette tâche, la section des transformations de texte sur la feuille de formes fournit les propriétés TxtPin, TxtLocPin, TxtWidth et TxtHeight. Les développeurs peuvent interagir avec ces propriétés par programmation en utilisant Aspose.Diagram API.

La section des transformations de texte contient les informations de position sur le bloc de texte d'une forme. Ces exemples montrent comment ajuster les positions du texte de forme et l'angle d'orientation :

- [Définir la position du texte de la forme en haut](/diagram/fr/java/working-with-text-boxes/).
- [Définir la position du texte de la forme en bas](/diagram/fr/java/working-with-text-boxes/).
- [Définir la position du texte de la forme à gauche](/diagram/fr/java/working-with-text-boxes/).
- [Définir la position du texte de la forme à droite](/diagram/fr/java/working-with-text-boxes/).
### **Définir la position du texte de la forme en haut**
Le morceau de code suivant définit l'angle d'orientation et la position du texte de la forme en haut.

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
### **Définir la position du texte de la forme en bas**
Le morceau de code suivant définit l'angle d'orientation et la position du texte de la forme en bas.

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
### **Définir la position du texte de la forme à gauche**
Le morceau de code suivant définit l'angle d'orientation et la position du texte de la forme à gauche.

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
### **Définir la position du texte de la forme à droite**
Le morceau de code suivant définit l'angle d'orientation et la position du texte de la forme à droite.

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
