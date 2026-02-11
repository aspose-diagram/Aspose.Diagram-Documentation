---
title: Visio-Shape-Daten hinzufügen, abrufen, kopieren und lesen
type: docs
weight: 10
url: /de/java/add-retrieve-copy-and-read-visio-shape-data/
description: In diesem Abschnitt wird erläutert, wie Sie eine Form hinzufügen, die Eigenschaften einer Form festlegen oder eine Form mit Aspose.Diagram kopieren.
---
## **Hinzufügen einer neuen Form in Visio**
Mit Aspose.Diagram for Java können Sie Microsoft Visio Diagramme auf verschiedene Weise bearbeiten. Eines der Dinge, die Sie tun können, ist das Hinzufügen neuer Formen zu einem Diagramm. Mit Aspose.Diagram for Java können Sie einer diagram eine neue Form hinzufügen. Die hinzugefügte Form kann auch mit Aspose.Diagram for Java angepasst werden.

In diesem Thema wird beschrieben, wie Sie einer diagram eine neue rechteckige Form hinzufügen.

Verwenden Sie Aspose.Diagram for Java API, um neue Formen zu erstellen, und fügen Sie diese Formen dann der Formensammlung von diagram hinzu.

So fügen Sie eine neue Form hinzu:

1. **Finde die Seite** - Jede Visio diagram enthält eine Sammlung von Seiten. Entwickler können die Seite nach Seiten-ID oder Name abrufen und die erforderliche Seite in der speichern[Buchseite](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)Klasse Objekt.
1. **Fügen Sie den erforderlichen Master einer Form hinzu** - Jeder Visio diagram enthält eine Sammlung von Meistern. Entwickler können einen Master (nach ID oder Name) aus der vorhandenen Schablonendatei (über direkten Pfad oder Dateistream) hinzufügen.
1. **Fügen Sie Form in Visio diagram hinzu** - Entwickler können eine neue Form im Visio diagram nach Seitenindex (beginnend bei 0), Hauptname, PinX, PinY, Höhe (optional) und Breite (optional) platzieren.
1. **Formeigenschaften festlegen** - AddShape-Methode der Klasse Diagram gibt die Shape-ID zurück. Entwickler können die Form von Visio diagram abrufen, indem sie diese ID verwenden, und dann ihre Eigenschaften festlegen, z. B. Farbe, Position, Ausrichtung und Text.

|<p>**Die Eingabe diagram** </p><p>![todo: Bild_alt_Text](add-retrieve-copy-and-read-visio-shape-data_1.png)</p>|<p>**Die diagram mit einer hinzugefügten Form** </p><p>![todo: Bild_alt_Text](add-retrieve-copy-and-read-visio-shape-data_2.png)</p>|
|:- |:- |
### **Programmierbeispiel hinzufügen**
Das folgende Code-Snippet zeigt, wie die einzelnen Schritte ausgeführt werden.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AddingNewShape.class);  
//Load a diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-2");

// Add master with stencil file path and master id
String masterName = "Rectangle";
// Add master with stencil file path and master name
diagram.addMaster(dataDir + "Basic Shapes.vss", masterName);
            
// page indexing starts from 0
int PageIndex = 1;
double width = 2, height = 2, pinX = 4.25, pinY = 4.5;
//Add a new rectangle shape
long rectangleId = diagram.addShape(pinX, pinY, width, height, masterName, PageIndex);
            
// set shape properties 
Shape rectangle = page.getShapes().getShape(rectangleId);
rectangle.getXForm().getPinX().setValue(5);
rectangle.getXForm().getPinY().setValue(5);
rectangle.setType(TypeValue.SHAPE);
rectangle.getText().getValue().add(new Txt("Aspose Diagram"));
rectangle.setTextStyle(diagram.getStyleSheets().get(3));
rectangle.getLine().getLineColor().setValue("#ff0000");
rectangle.getLine().getLineWeight().setValue(0.03);
rectangle.getLine().getRounding().setValue(0.1);
rectangle.getFill().getFillBkgnd().setValue("#ff00ff");
rectangle.getFill().getFillForegnd().setValue("#ebf8df");

diagram.save(dataDir + "AddShape_Out.vsdx", SaveFileFormat.VSDX);
System.out.println("Shape has been added.");

{{< /highlight >}}


{{% alert color="primary" %}}

 Wir freuen uns über Ihre Fragen und Anregungen unter[Aspose.Diagram Forum](https://forum.aspose.com/c/diagram/17). Wir antworten umgehend.

{{% /alert %}}
## **Forminformationen abrufen**
[Arbeiten mit Diagrammen](/diagram/de/java/working-with-diagrams/)erklärt, wie man Diagramme erstellt, Formen und Verbinder hinzufügt und dann Informationen über diagram-Elemente wie z[Seiten](/diagram/de/java/retrieve-get-copy-and-insert-a-page/), [Meister](https://docs.aspose.com/diagram/java/working-with-masters/), [Anschlüsse](https://reference.aspose.com/diagram/java/com.aspose.diagram/ConnectCollection) und[Schriftarten](https://reference.aspose.com/diagram/java/com.aspose.diagram/FontCollection). In diesem Artikel wird beschrieben, wie Sie Informationen zu Formen in einem diagram abrufen.

Jede Form in einem diagram hat eine ID und einen Namen. Die ID ist beim Programmieren mit Visio wichtig: Sie ist die Hauptmethode für den Zugriff auf eine Form. Jede Form enthält auch Informationen darüber, aus welchem Master (Schablone) sie besteht.

 EIN[Form](http://www.aspose.com/api/java/diagram/com.aspose.diagram/shape) ist ein Objekt in einer Visio-Zeichnung. Die Shapes-Eigenschaft, die von der Page-Klasse verfügbar gemacht wird, unterstützt eine Sammlung von Aspose.Diagram.Shape-Objekten. Die Shapes-Eigenschaft kann verwendet werden, um Informationen zu einer Form abzurufen.

Im Konsolenfenster unten sehen Sie beispielsweise die Informationsausgabe für diagram, die vier Shapes enthielt: zwei Terminatoren, einen Prozess und einen dynamischen Konnektor. Jedes hat eine eindeutige ID sowie den Namen der Master-Form (Schablone).

|**Ein Konsolenfenster mit Shape-Informationen**|
|:- |
|![todo: Bild_alt_Text](add-retrieve-copy-and-read-visio-shape-data_3.png)|
So rufen Sie Visio-Seiteninformationen ab:

1. Lädt eine diagram.
1. Richtet eine Foreach-Schleife ein, um alle Formen in diagram zu durchlaufen.
1. Zeigt Forminformationen an.
### **Programmierbeispiel abrufen**
Der folgende Codeabschnitt ruft die Forminformationen von Visio diagram ab.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RetrieveShapeInfo.class);

//Load diagram
Diagram diagram = new Diagram(dataDir+ "RetrieveShapeInfo.vsd");

for (com.aspose.diagram.Shape shape : (Iterable<Shape>) diagram.getPages().getPage(0).getShapes())
{
    //Display information about the shapes
    System.out.println("\nShape ID : " + shape.getID());
    System.out.println("Name : " + shape.getName());
    System.out.println("Master Shape : " + shape.getMaster().getName());
}

{{< /highlight >}}


## **Kopieren Sie Formen von einem vorhandenen Visio**
Aspose.Diagram for Java API ermöglicht es Entwicklern, Formen von der Quellseite Visio auf die neue Seite Visio diagram zu kopieren. Es unterstützt auch das Kopieren von Gruppenformen. Dieser Artikel beschreibt, wie Sie alle Shapes von der Quellseite diagram kopieren.

Um Formen zu kopieren, sollten Entwickler auch Quell-PageSheet- und Quell-Visio-Designs kopieren, um den Formfüllstil und andere Formatierungseigenschaften beizubehalten.

Dieses Beispiel funktioniert wie folgt:

1. Laden Sie eine Quelle Visio.
1. Initialisieren Sie eine neue Visio
1. Fügen Sie Master und Themen aus der Quelle Visio hinzu.
1. Rufen Sie die Seite von der Quelle Visio ab.
1. Kopieren Sie sein PageSheet auf die neue Seite Visio.
1. Iterieren Sie durch die Formen der Quellseite Visio.
1. Legen Sie die neue ID fest und fügen Sie sie der neuen Seite Visio hinzu.
1. Speichern Sie die neue Visio im lokalen Speicher.
### **Programmierbeispiel kopieren**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CopyShape.class); 
// load a source Visio
Diagram srcVisio = new Diagram(dataDir + "Drawing1.vsdx");
        
// initialize a new Visio
Diagram newDiagram = new Diagram();

// add all masters from the source Visio diagram
MasterCollection originalMasters = srcVisio.getMasters();
for (Master master : (Iterable<Master>) originalMasters)
    newDiagram.addMaster(srcVisio, master.getName());

// get the page object from the original diagram
Page SrcPage = srcVisio.getPages().getPage("Page-1");
// copy themes from the source diagram
newDiagram.copyTheme(srcVisio);
// copy pagesheet of the source Visio page
newDiagram.getPages().get(0).getPageSheet().copy(SrcPage.getPageSheet());

// copy shapes from the source Visio page
for (Shape shape :(Iterable<Shape>) SrcPage.getShapes())
{
    newDiagram.getPages().get(0).getShapes().add(shape);
}
// save the new Visio
newDiagram.save(dataDir + "CopyShapes_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}



{{% alert color="primary" %}}

 Wir freuen uns über Ihre Fragen und Anregungen unter[Aspose.Diagram Forum](https://forum.aspose.com/c/diagram/17). Wir antworten umgehend.

{{% /alert %}}
## **Kopieren Sie eine Visio-Form in eine andere Forminstanz**
Die Copy-Methode der Shape-Klasse nimmt eine Shape-Instanz zum Klonen.

## **Lesen von Visio Formdaten**
 Die Props-Sammlung, die von der bereitgestellt wird[Form](http://www.aspose.com/api/java/diagram/com.aspose.diagram/shape) Klasse unterstützt die[Aspose.Diagram.Prop](http://www.aspose.com/api/java/diagram/com.aspose.diagram/prop) Objekt. Die Eigenschaft kann verwendet werden, um die Daten einer Form (benutzerdefinierte Eigenschaften) zu lesen.
### **Lesen Sie alle Shape-Eigenschaften**
So identifizieren Sie benutzerdefinierte Eigenschaften in Microsoft Visio:

1. Klicken Sie in einem diagram mit der rechten Maustaste auf eine Form.
1.  Auswählen**Daten** , dann**Shape-Daten** aus dem Menü.
 Alle vorhandenen Eigenschaften werden im Dialogfeld aufgelistet.

|**Die Daten einer Form, wie in Microsoft Visio zu sehen.**|** |
|:- |:- |
|![todo: Bild_alt_Text](add-retrieve-copy-and-read-visio-shape-data_4.png)||


|**Ein Konsolenfenster, das die Shape-Datenausgabe anzeigt.**|** |
|:- |:- |
|![todo: Bild_alt_Text](add-retrieve-copy-and-read-visio-shape-data_5.png)||
#### **Programmierbeispiel lesen**
Die folgenden Codeausschnitte lesen Formdaten (benutzerdefinierte Eigenschaften).


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ReadAllShapeProps.class);  

// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-3");

for (Shape shape :(Iterable<Shape>) page.getShapes())
{
    if (shape.getName() == "Process1")
    {
        for (Prop property :(Iterable<Prop>) shape.getProps())
        {
            System.out.println(property.getLabel().getValue() + ": " + property.getValue().getVal());
        }
        break;
    }
}

{{< /highlight >}}


### **Lesen Sie eine Shape-Eigenschaft nach Namen**
Das folgende Code-Snippet liest eine Shape-Eigenschaft nach Namen (benutzerdefinierte Eigenschaft).
#### **Read by Name Programmierbeispiel**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ReadShapePropByName.class);   
// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-3");

for (Shape shape :(Iterable<Shape>) page.getShapes())
{
    if (shape.getName() == "Process1")
    {
        Prop property = shape.getProps().getProp("Name1");
        System.out.println(property.getLabel().getValue() + ": " + property.getValue().getVal());
    }
}

{{< /highlight >}}


## **Verwenden Sie Verbindungsindizes, um Shapes zu verbinden**
Aspose.Diagram for Java API ermöglicht es Entwicklern bereits, neue Verbindungspunkte auf der Form hinzuzufügen, und Entwickler können jetzt Formen mithilfe von Verbindungsindizes verbinden.
### **Verwenden Sie Verbindungsindizes, um Shapes zu verbinden**
Das ConnectShapesViaConnectorIndex-Member, das von verfügbar gemacht wird[Buchseite](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)-Klasse kann verwendet werden, um Shapes mithilfe von Verbindungsindizes zu verbinden.

1. Initialisieren Sie eine neue Zeichnung.
1. Platziere vier rechteckige Formen
1. Fügen Sie zwei zusätzliche Verbindungspunkte hinzu, sodass sich auf der unteren Begrenzungslinie drei Verbindungspunkte befinden würden
1. Verbinden Sie die erste Form von jeder unteren Verbindung mit anderen drei rechteckigen Formen von oben mit dynamischen Verbindern
1. Zeichnung speichern
#### **Verwenden Sie Verbindungsindizes, um Shapes zu verbinden Programmierbeispiel**
Verwenden Sie den folgenden Code in Ihrer Java-Anwendung, um Shapes mithilfe von Verbindungsindizes mit Aspose.Diagram for Java API zu verbinden.

## **Rufen Sie die übergeordnete Form einer untergeordneten Form ab**
Aspose.Diagram for Java ermöglicht Entwicklern das Abrufen der übergeordneten Form einer Unterform.
### **Holen Sie sich die übergeordnete Form**
Das[Form](http://www.aspose.com/api/java/diagram/com.aspose.diagram/shape)Die Klasse bietet die ParentShape-Eigenschaft zum Abrufen der übergeordneten Form.
#### **Holen Sie sich das Programmierbeispiel für übergeordnete Formen**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveTheParentShape.class) + "Shapes\\";
		
// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a sub-shape by page name, group shape ID, and then sub-shape ID
Shape shape = diagram.getPages().getPage("Page-3").getShapes().getShape(13).getShapes().getShape(2);
Shape parentShape = shape.getParentShape();
System.out.println("Parent Shape's Properties:");
System.out.println("Shape ID: " + parentShape.getID());
System.out.println("Shape Name: " + parentShape.getName());
System.out.println("Shape Type: " + parentShape.getType());
{{< /highlight >}}


