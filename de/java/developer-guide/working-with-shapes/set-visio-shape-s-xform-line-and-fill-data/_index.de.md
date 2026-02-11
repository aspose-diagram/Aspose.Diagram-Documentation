---
title: Legen Sie die XForm-, Linien- und Fülldaten von Visio Form fest
type: docs
weight: 70
url: /de/java/set-visio-shape-s-xform-line-and-fill-data/
---
## **Festlegen von XForm-Daten**
 Das XForm-Element ist Teil des XML-Schemas Microsoft Visio. XForm gibt die Position einer Form an, z. B. Breite, Höhe, Drehung und ob die Form gespiegelt wurde. Das[XForm](https://reference.aspose.com/diagram/java/com.aspose.diagram/xform) Eigentum, ausgesetzt durch die[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) Klasse, unterstützt das Objekt Aspose.Diagram.XForm. Die XForm-Eigenschaft kann verwendet werden, um die XForm-Daten einer Form abzurufen oder zu aktualisieren. Die Codebeispiele in diesem Artikel ändern die XForm-Werte PinX (X-Koordinate) und PinY (Y-Koordinate), um die Shapes auf der Seite zu verschieben.

**Geben Sie diagram ein** 

![todo: Bild_alt_Text](set-visio-shape-s-xform-line-and-fill-data_1.png)

**Die diagram nach der** **PinX** **und** **PinY** **Werte wurden geändert** 

![todo: Bild_alt_Text](set-visio-shape-s-xform-line-and-fill-data_2.png)

Der Prozess zum Aktualisieren von XForm-Daten ist:

1. Laden Sie ein diagram.# Finden Sie eine bestimmte Form.# Aktualisieren Sie die XForm-Daten der Form.
1. Speichern Sie die diagram.
### **Programmierbeispiel**
Das folgende Code-Snippet zeigt, wie die XForm-Daten einer Form aktualisiert werden. Der Code sucht nach einem Shape-Namensprozess mit der Shape-ID 1 und setzt seine X- und Y-Koordinaten auf 5.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetXFormdata.class); 
// call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "SetXFormdata.vsd");

//Find a particular shape and update its XForm
for(Shape shape :(Iterable<Shape>) diagram.getPages().get(0).getShapes())
{
    if (shape.getNameU().toLowerCase() == "process" && shape.getID() == 1)
    {
        shape.getXForm().getPinX().setValue(5);
        shape.getXForm().getPinY().setValue(5);
    }
}
// save diagram
diagram.save(dataDir + "SetXFormdata_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Legen Sie die Liniendaten der Form Visio fest**
Formen können auf verschiedene Arten formatiert werden. Dieser Artikel zeigt, wie Sie die Attribute einer Linie angeben.

Microsoft Visio lässt Benutzer Linien auf verschiedene Arten formatieren. Aspose.Diagram for Java unterstützt:

- Gewicht: die Dicke einer Linie.
- Farbe: Legen Sie die Linienfarbe der Form fest.
- Transparenz der Linienfarbe: Legen Sie die Transparenz der Linienfarbe der Form in Prozent fest.
- Muster: legt fest, ob die Linie durchgezogen, gestrichelt oder mit einem anderen Muster ist.
- Rundung: der Radius der Ecken.
- Anfangs- und Endpfeile: Gibt an, ob die Linie Pfeile hat.
- Anfangs- und Endpfeilgröße: Legen Sie die Pfeilgröße fest.
- Kappe: die Rundung der Linienenden.
### **Ändern Sie die Linienfarbe, das Gewicht, den Strichtyp, die Transparenz, die Rundung, den Pfeiltyp und die Pfeilgröße des Rahmens einer Form**
 Das[Linie](https://reference.aspose.com/diagram/java/com.aspose.diagram/line) Eigentum, ausgesetzt durch die[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)Klasse, unterstützt das Objekt Aspose.Diagram.Line. Diese Eigenschaft kann verwendet werden, um die Liniendaten einer Form abzurufen oder zu aktualisieren.
#### **Programmierbeispiel für Leitungsdaten**
Der folgende Codeabschnitt aktualisiert die Liniendaten von shape.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetLineData.class);

// load a Visio diagram
Diagram diagram = new Diagram(dataDir + "SetLineData.vsd");
// get the page by its name
Page page1 = diagram.getPages().getPage("Page-1");
// get shape by its ID
Shape shape = page1.getShapes().getShape(1);
// set line dash type by index
shape.getLine().getLinePattern().setValue(4);
// set line weight, defualt in PT
shape.getLine().getLineWeight().setValue(2);
// set color of the shape's line
shape.getLine().getLineColor().getUfe().setF("RGB(95,108,53)");
// set line rounding, default in inch
shape.getLine().getRounding().setValue(0.3125);
// set line caps
shape.getLine().getLineCap().setValue(BOOL.TRUE);
// set line color transparency in percent
shape.getLine().getLineColorTrans().setValue(50);

/* add arrows to the connector or curve shapes */
// select arrow type by index
shape.getLine().getBeginArrow().setValue(4);
shape.getLine().getEndArrow().setValue(4);
// set arrow size 
shape.getLine().getBeginArrowSize().setValue(ArrowSizeValue.LARGE);
shape.getLine().getBeginArrowSize().setValue(ArrowSizeValue.LARGE);

// save the Visio
diagram.save(dataDir + "SetLineData_Out.vsdx", SaveFileFormat.VSDX);
// save diagram
diagram.save(dataDir+ "output.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
## **Legen Sie die Fülldaten der Form Visio fest**
Formen können auf verschiedene Arten formatiert werden. In diesem Thema wird beschrieben, wie Sie die Füllung einer Form angeben.

 Microsoft Office Visio lässt Benutzer Füllungen auf verschiedene Weise formatieren. Das[Füllen](https://reference.aspose.com/diagram/java/com.aspose.diagram/fill) Klasse der Aspose.Diagram for Java API unterstützt Einstellung:

- Hintergrund- und Vordergrundfarben.
- Transparenz.
- Muster füllen.
- Schatten.
### **Füllwerte einstellen**
Die Fill-Eigenschaft, die von der Shape-Klasse verfügbar gemacht wird, unterstützt das Aspose.Diagram.Fill-Objekt. Die Fill-Eigenschaft kann verwendet werden, um die Fülldaten einer Form abzurufen oder zu aktualisieren.

|<p>**Die Eingabe diagram** </p><p>![todo: Bild_alt_Text](http://i.imgur.com/OrhEecb.png)</p>|<p>**Die diagram nach dem Ändern der Füllfarbe** </p><p>![todo: Bild_alt_Text](http://i.imgur.com/HO0wmZ8.png)</p>|
|:- |:- |
#### **Füllen Sie das Programmierbeispiel für Daten aus**
Der folgende Codeausschnitt aktualisiert die Fülldaten einer Form. Der Code sucht nach einer Form namens Rechteck mit der Form-ID 1 und legt die Hintergrund- und Vordergrundfarben für die Füllung fest.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetFillData.class);


//Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir+ "Drawing1.vsd");

//Find a particular shape and update its XForm
for (com.aspose.diagram.Shape shape : (Iterable<Shape>) diagram.getPages().get(0).getShapes())
{
    if (shape.getNameU().toLowerCase() == "rectangle" && shape.getID() == 1)
    {
        shape.getFill().getFillBkgnd().setValue(diagram.getPages().getPage(0).getShapes().getShape(0).getFill().getFillBkgnd().getValue());
        shape.getFill().getFillForegnd().setValue("#ebf8df");
    }
}
// save diagram
diagram.save(dataDir+ "SetFillData_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
### **Rufen Sie geerbte Fülldaten einer Visio-Form ab**
Die Formen Visio können den übergeordneten Stil und die Masterform erben. Entwickler können die vererbten Fülldaten einer Visio-Form abrufen oder festlegen. Die InheritFill-Eigenschaft, die von der Shape-Klasse verfügbar gemacht wird, enthält die Füllungsformatierungswerte für die Form, die vom übergeordneten Stil und der Masterform geerbt werden.
#### **Programmierbeispiel für geerbte Fülldaten abrufen**
Der folgende Codeausschnitt ruft die geerbten Fülldaten der Form ab. Bitte überprüfen Sie diesen Beispielcode:

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveInheritedFillData.class) + "Shapes/";

// Call the diagram constructor to load a VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get page by ID
Page page = diagram.getPages().getPage("Page-1");
// Get shape by ID
Shape shape = page.getShapes().getShape(1);
// Get the fill formatting values
System.out.println(shape.getInheritFill().getFillBkgnd().getValue());
System.out.println(shape.getInheritFill().getFillForegnd().getValue());
System.out.println(shape.getInheritFill().getFillPattern().getValue());
System.out.println(shape.getInheritFill().getShapeShdwObliqueAngle().getValue());
System.out.println(shape.getInheritFill().getShapeShdwOffsetX().getValue());
System.out.println(shape.getInheritFill().getShapeShdwOffsetY().getValue());
System.out.println(shape.getInheritFill().getShapeShdwScaleFactor().getValue());
System.out.println(shape.getInheritFill().getShapeShdwType().getValue());
System.out.println(shape.getInheritFill().getShdwBkgnd().getValue());
System.out.println(shape.getInheritFill().getShdwBkgndTrans().getValue());
System.out.println(shape.getInheritFill().getShdwForegnd().getValue());
System.out.println(shape.getInheritFill().getShdwForegndTrans().getValue());
System.out.println(shape.getInheritFill().getShdwPattern().getValue());

{{< /highlight >}}
```
