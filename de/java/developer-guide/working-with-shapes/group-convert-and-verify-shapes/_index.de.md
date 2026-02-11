---
title: Formen gruppieren, konvertieren und überprüfen
type: docs
weight: 50
url: /de/java/group-convert-and-verify-shapes/
---
## **Gruppieren Sie mehrere Formen in der Zeichnung Visio**
Aspose.Diagram API ermöglicht es Entwicklern, Formen zu gruppieren, um sie alle auf einmal zu verschieben. Jede Form in einer Gruppe behält eine eindeutige Identität bei und hat ihre eigenen Eigenschaften. Wenn wir die Formatierung einer Gruppe von Formen ändern, weist sie jeder Form die neue Eigenschaft zu.
### **So gruppieren Sie Formen**
Die Group-Methode, die von der ShapeCollection-Klasse verfügbar gemacht wird, kann verwendet werden, um Formen zu gruppieren.

Der folgende Code zeigt, wie man:

1. Laden Sie eine Probe diagram.
1. initialisierte ein Array der Formen
1. Holen Sie sich eine bestimmte Form nach ID.
1. Holen Sie sich eine andere bestimmte bestimmte Form nach ID.
1. Weisen Sie dem Array Shapes zu.
1. gruppieren Sie Shapes, indem Sie die Group-Methode aufrufen.
1. außer diagram
#### **Programmierbeispiel für Gruppenformen**
Verwenden Sie den folgenden Code in Ihrer Java-Anwendung, um Formen mit Aspose.Diagram for Java API zu gruppieren.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GroupShapes.class);
// load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-3");

// Initialize an array of shapes
Shape[] ss = new Shape[3];

// extract and assign shapes to the array
ss[0] = page.getShapes().getShape(15);
ss[1] = page.getShapes().getShape(16);
ss[2] = page.getShapes().getShape(17);

// mark array shapes as group
page.getShapes().group(ss);

// save visio diagram
diagram.save(dataDir + "GroupShapes_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Konvertieren Sie eine Visio-Form in andere Dateiformate**
Aspose.Diagram for Java API ermöglicht es Entwicklern, eine einzelne Visio-Form in jedes andere unterstützte Dateiformat zu konvertieren. In diesem Artikel entfernen wir alle anderen Visio-Shapes von der Seite und passen die Seiteneinstellungen entsprechend der Quell-Shape-Größe an.
### **Konvertieren einer bestimmten Visio-Form**
Developers can convert a Visio shape to PDF, HTML, Image, SVG, and SWF by [Angabe der Visio Speicheroptionen]().
Dieser Beispielcode funktioniert wie folgt:

1. Laden Sie eine Quelle Visio.
1. Holen Sie sich eine bestimmte Seite.
1. Entfernen Sie die Hintergrundseite.
1. Erstellen Sie eine Hash-Tabelle aller Formen, die die IDs und Namen enthalten.
1. Durchlaufen Sie die Hash-Tabelle
1. Entfernen Sie alle Formen von der Seite Visio, außer der bestimmten.
1. Legen Sie die Seitengröße fest.
1. Speichern Sie die Seite Visio in einem beliebigen unterstützten Dateiformat.
#### **Konvertieren Sie Shape-Programmierbeispiel**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SaveVisioShapeInOtherFormats.class);   
        
double shapeWidth = 0;
double shapeHeight = 0;

// call a Diagram class constructor to load the VSDX diagram
Diagram srcVisio = new Diagram(dataDir + "Drawing1.vsdx");
// get Visio page
Page srcPage = srcVisio.getPages().get(1);
// remove background page
srcPage.setBackPage(null);

// get hash table of shapes, it holds id and name
Hashtable<Long, String> remShapes = new Hashtable<Long, String>();
for (Shape shape : (Iterable<Shape>)srcPage.getShapes())
    // for the normal shape
    remShapes.put(shape.getID(), shape.getName());
        

// iterate through the hash table
Enumeration<Long> enumKey = remShapes.keys();
while(enumKey.hasMoreElements())
{
    Long key = enumKey.nextElement();
    String val = remShapes.get(key);
    Shape shape = srcPage.getShapes().getShape(key);
    // check of the shape name
    if(val.equals("GroupShape1"))
    {
        // move shape to the origin corner
        shapeWidth = shape.getXForm().getWidth().getValue();
        shapeHeight = shape.getXForm().getHeight().getValue();
        shape.moveTo(shapeWidth*0.5, shapeHeight*0.5);
        // trim page size
        srcPage.getPageSheet().getPageProps().getPageWidth().setValue(shapeWidth);
        srcPage.getPageSheet().getPageProps().getPageHeight().setValue(shapeHeight);
    }
    else
    {
        // remove shape from the Visio page and hash table
        srcPage.getShapes().remove(shape);
        remShapes.remove(key);
    }
}

// specify saving options
PdfSaveOptions opts = new PdfSaveOptions();
// set page count to save
opts.setPageCount(1);
// set starting index of the page
opts.setPageIndex(1);
// save it
srcVisio.save(dataDir + "SaveVisioShapeInOtherFormats_Out.pdf", opts);

{{< /highlight >}}
```
### **Convert Visio Shape to PDF**
The ToPdf method of the Shape class allows to convert a shape into the PDF format.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toPdf(dataDir + "out.pdf");

{{< /highlight >}}
### **Convert Visio Shape to HTML**
The ToHTML method of the Shape class allows to convert a shape into the HTML format.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

HTMLSaveOptions hs = new HTMLSaveOptions();

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toHTML(dataDir + "out.pdf", hs);

{{< /highlight >}}

{{% alert color="primary" %}} 

 Wir freuen uns über Ihre Fragen und Anregungen unter[Aspose.Diagram Forum](https://forum.aspose.com/c/diagram/17). Wir antworten umgehend.

{{% /alert %}} 
## **Überprüfen Sie, ob zwei Visio-Formen verbunden oder geklebt sind**
 Mit Aspose.Diagram for Java API können Entwickler überprüfen, ob die beiden Formen Visio verklebt oder verbunden sind. Zuvor haben wir in diesen Hilfethemen gesehen, wie wir zwei Formen verbinden oder kleben können:[Visio Formen hinzufügen und verbinden](/diagram/de/java/add-and-connect-visio-shapes/) und[Kleben Sie Formen in den Behälter](/diagram/de/java/working-with-shapes-gluing/).
### **Überprüfung der verbundenen oder geklebten Formen**
 Das[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) Die Klasse bietet IsGlued- und IsConnected-Eigenschaften, um zu bestimmen, ob zwei Shapes geklebt oder verbunden sind.
#### **Programmierbeispiel für verbundene oder geklebte Formen**
Der folgende Codeabschnitt überprüft, ob zwei Shapes verbunden oder geklebt sind.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(VerifyConnectedOrGluedShapes.class);  
// call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// set two shape ids
long ShapeIdOne = 15;
long ShapeIdTwo = 16;

// get Visio page by name
Page page = diagram.getPages().getPage("Page-3");

// get Visio shapes by ids
Shape ShapedOne = page.getShapes().getShape(ShapeIdOne);
Shape ShapedTwo = page.getShapes().getShape(ShapeIdTwo);

// determine whether shapes are connected
boolean connected = ShapedOne.isConnected(ShapedTwo);
System.out.println("Shapes are connected: " + connected);

// determine whether shapes are glued
boolean glued = ShapedOne.isGlued(ShapedTwo);
System.out.println("Shapes are Glued: " + glued);

{{< /highlight >}}
```
## **Überprüfen Sie, ob sich die Form Visio in einer Gruppe von Formen befindet**
Mit Aspose.Diagram for Java API können Entwickler überprüfen, ob sich die Form Visio in einer Gruppe von Formen befindet oder nicht.
### **Überprüfung der Form in der Gruppe der Formen**
Die Shape-Klasse bietet IsInGroup-Eigenschaften, um zu bestimmen, ob sich das Visio-Shape in einem Gruppen-Shape befindet.
#### **Überprüfung der Form in der Gruppe von Formen Programmierbeispiel**
Der folgende Codeabschnitt überprüft, ob sich das Shape in einem Gruppen-Shape befindet.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveTheParentShape.class) + "Shapes\\";
				
// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a sub-shape by page name, group shape ID, and then sub-shape ID
Shape shape = diagram.getPages().getPage("Page-3").getShapes().getShape(13).getShapes().getShape(2);
System.out.println("Is it in a Group: " + shape.isInGroup());
{{< /highlight >}}
```

{{% alert color="primary" %}} 

 Wir freuen uns über Ihre Fragen und Anregungen unter[Aspose.Diagram Forum](https://forum.aspose.com/c/diagram/17). Wir antworten umgehend.

{{% /alert %}}
