---
title: Arbeiten mit Visio Shape-Daten
type: docs
weight: 30
url: /de/java/working-with-visio-shape-data/
---
## **Hinzufügen einer neuen Form in Visio**
Mit Aspose.Diagram for Java können Sie Microsoft Visio Diagramme auf verschiedene Weise bearbeiten. Eines der Dinge, die Sie tun können, ist das Hinzufügen neuer Formen zu einem Diagramm. Mit Aspose.Diagram for Java können Sie einer diagram eine neue Form hinzufügen. Die hinzugefügte Form kann auch mit Aspose.Diagram for Java angepasst werden.

In diesem Thema wird beschrieben, wie Sie einer diagram eine neue rechteckige Form hinzufügen.

Verwenden Sie die API von Aspose.Diagram for Java, um neue Formen zu erstellen, und fügen Sie diese Formen dann der Formensammlung von diagram hinzu.

So fügen Sie eine neue Form hinzu:

1. **Finde die Seite** - Jede Visio diagram enthält eine Sammlung von Seiten. Entwickler können die Seite nach Seiten-ID oder Name abrufen und die erforderliche Seite in der speichern[Buchseite](https://reference.aspose.com/diagram//java/com.aspose.diagram/page)Klasse Objekt.
1. **Fügen Sie den erforderlichen Master einer Form hinzu** - Jeder Visio diagram enthält eine Sammlung von Meistern. Entwickler können einen Master (nach ID oder Name) aus der vorhandenen Schablonendatei (über direkten Pfad oder Dateistream) hinzufügen.
1. **Fügen Sie Form in Visio diagram hinzu** - Entwickler können eine neue Form im Visio diagram nach Seitenindex (beginnend bei 0), Hauptname, PinX, PinY, Höhe (optional) und Breite (optional) platzieren.
1. **Formeigenschaften festlegen** - AddShape-Methode der Klasse Diagram gibt die Shape-ID zurück. Entwickler können die Form von Visio diagram abrufen, indem sie diese ID verwenden, und dann ihre Eigenschaften festlegen, z. B. Farbe, Position, Ausrichtung und Text.

|<p>**Die Eingabe diagram** </p><p>![todo: Bild_alt_Text](working-with-visio-shape-data_1.png)</p>|<p>**Die diagram mit einer hinzugefügten Form** </p><p>![todo: Bild_alt_Text](working-with-visio-shape-data_2.png)</p>|
|:- |:- |
### **Programmierbeispiel hinzufügen**
Das folgende Code-Snippet zeigt, wie die einzelnen Schritte ausgeführt werden.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-AddingNewShape-AddingNewShape.java" >}}

{{% alert color="primary" %}}

 Wir freuen uns über Ihre Fragen und Anregungen unter[Aspose.Diagram Forum](https://forum.aspose.com/c/diagram/17). Wir antworten umgehend.

{{% /alert %}}
## **Forminformationen abrufen**
[Arbeiten mit Diagrammen](/diagram/de/java/working-with-diagrams/)erklärt, wie man Diagramme erstellt, Formen und Verbinder hinzufügt und dann Informationen über diagram-Elemente wie z[Seiten](/diagram/de/java/retrieve-get-copy-and-insert-a-page/), [Meister](/diagram/de/java/working-with-masters/) , Anschlüsse u[Schriftarten](/diagram/de/java/aspose-diagram-font-operations/). In diesem Artikel wird beschrieben, wie Sie Informationen zu Formen in einem diagram abrufen.

Jede Form in einem diagram hat eine ID und einen Namen. Die ID ist beim Programmieren mit Visio wichtig: Sie ist die Hauptmethode für den Zugriff auf eine Form. Jede Form enthält auch Informationen darüber, aus welchem Master (Schablone) sie besteht.

 EIN[Form](https://reference.aspose.com/diagram//java/com.aspose.diagram/shape) ist ein Objekt in einer Visio-Zeichnung. Die Shapes-Eigenschaft, die von der Page-Klasse verfügbar gemacht wird, unterstützt eine Sammlung von Aspose.Diagram.Shape-Objekten. Die Shapes-Eigenschaft kann verwendet werden, um Informationen zu einer Form abzurufen.

Im Konsolenfenster unten sehen Sie beispielsweise die Informationsausgabe für diagram, die vier Shapes enthielt: zwei Terminatoren, einen Prozess und einen dynamischen Konnektor. Jedes hat eine eindeutige ID sowie den Namen der Master-Form (Schablone).

**Ein Konsolenfenster mit Shape-Informationen**

![todo: Bild_alt_Text](working-with-visio-shape-data_3.png)

So rufen Sie Visio-Seiteninformationen ab:

1. Lädt eine diagram.
1. Richtet eine Foreach-Schleife ein, um alle Formen in diagram zu durchlaufen.
1. Zeigt Forminformationen an.
### **Programmierbeispiel abrufen**
Der folgende Codeabschnitt ruft die Forminformationen von Visio diagram ab.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-RetrieveShapeInfo-RetrieveShapeInfo.java" >}}
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
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-CopyShape-CopyShape.java" >}}

{{% alert color="primary" %}}

 Wir freuen uns über Ihre Fragen und Anregungen unter[Aspose.Diagram Forum](https://forum.aspose.com/c/diagram/17). Wir antworten umgehend.

{{% /alert %}}
## **Kopieren Sie eine Visio-Form in eine andere Forminstanz**
Die copy-Methode der Shape-Klasse nimmt eine Shape-Instanz zum Klonen.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Shape newShape = new Shape();

// copy diagram

newShape.copy(diagram.getPages().get(0).getShapes().get(0));

newShape.setID(3);

newShape.getXForm().getPinX().setValue(1);

newShape.getXForm().getPinY().setValue(1);

{{< /highlight >}}
## **Lesen von Visio Formdaten**
 Die von der Shape-Klasse verfügbar gemachte Props-Auflistung unterstützt die[Aspose.Diagram.Prop](https://reference.aspose.com/diagram//java/com.aspose.diagram/prop) Objekt. Die Eigenschaft kann verwendet werden, um die Daten einer Form (benutzerdefinierte Eigenschaften) zu lesen.
### **Lesen Sie alle Shape-Eigenschaften**
So identifizieren Sie benutzerdefinierte Eigenschaften in Microsoft Visio:

1. Klicken Sie in einem diagram mit der rechten Maustaste auf eine Form.
1.  Auswählen**Daten** , dann**Shape-Daten** aus dem Menü.
 Alle vorhandenen Eigenschaften werden im Dialogfeld aufgelistet.

|**Die Daten einer Form, wie in Microsoft Visio zu sehen.**|** |
|:- |:- |
|![todo: Bild_alt_Text](http://i.imgur.com/2loM7b0.png)||


|**Ein Konsolenfenster, das die Shape-Datenausgabe anzeigt.**|** |
|:- |:- |
|![todo: Bild_alt_Text](http://i.imgur.com/kmAKNrx.png)||
#### **Programmierbeispiel lesen**
Die folgenden Codeausschnitte lesen Formdaten (benutzerdefinierte Eigenschaften).

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-ReadAllShapeProps-ReadAllShapeProps.java" >}}
### **Lesen Sie eine Shape-Eigenschaft nach Namen**
Das folgende Code-Snippet liest eine Shape-Eigenschaft nach Namen (benutzerdefinierte Eigenschaft).
#### **Read by Name Programmierbeispiel**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-ReadShapePropByName-ReadShapePropByName.java" >}}
## **Verwenden Sie Verbindungsindizes, um Shapes zu verbinden**
Aspose.Diagram for Java API ermöglicht es Entwicklern bereits, neue Verbindungspunkte auf der Form hinzuzufügen, und Entwickler können jetzt Formen mithilfe von Verbindungsindizes verbinden.
### **Verwenden Sie Verbindungsindizes, um Shapes zu verbinden**
Das von der Page-Klasse verfügbar gemachte Mitglied connectShapesViaConnectorIndex kann verwendet werden, um Shapes mithilfe von Verbindungsindizes zu verbinden. Der folgende Code zeigt, wie Shapes verbunden werden:

1. Initialisieren Sie eine neue Zeichnung.
1. Platziere vier rechteckige Formen
1. Fügen Sie zwei zusätzliche Verbindungspunkte hinzu, sodass sich auf der unteren Begrenzungslinie drei Verbindungspunkte befinden würden
1. Verbinden Sie die erste Form von jeder unteren Verbindung mit anderen drei rechteckigen Formen von oben mit dynamischen Verbindern
1. Zeichnung speichern
#### **Verwenden Sie Verbindungsindizes, um Shapes zu verbinden Programmierbeispiel**
Verwenden Sie den folgenden Code in Ihrer Java-Anwendung, um Shapes mithilfe von Verbindungsindizes mit Aspose.Diagram for Java API zu verbinden.

**Java**

{{< highlight "java" >}}

 // initialize a new drawing

Diagram diagram = new Diagram();

// get page by index

Page page = diagram.getPages().get(0);

// add masters

String connectorMaster = "Dynamic connector", rectangle = "Rectangle";

int pageNumber = 0;

double width = 2, height = 2, pinX = 4.25, pinY = 9.5;

diagram.addMaster("C:\\temp\\Basic Shapes.vss", rectangle);

diagram.addMaster("C:\\temp\\Basic Shapes.vss", connectorMaster);

// add shapes

long shape1_ID = diagram.addShape(4.5, 7, rectangle, pageNumber);

long shape2_ID = diagram.addShape(2.25, 4.5, rectangle, pageNumber);

long shape3_ID = diagram.addShape(4.5, 4.5, rectangle, pageNumber);

long shape4_ID = diagram.addShape(6.75, 4.5, rectangle, pageNumber);

// get shapes by ID

Shape shape1 = page.getShapes().getShape(shape1_ID);

Shape shape2 = page.getShapes().getShape(shape2_ID);

Shape shape3 = page.getShapes().getShape(shape3_ID);

Shape shape4 = page.getShapes().getShape(shape4_ID);

// add two more connection points

Connection connection1 = new Connection();

connection1.getX().getUfe().setF("Width*0.33");

connection1.getY().getUfe().setF("Height*0");

Connection connection3 = new Connection();

connection3.getX().getUfe().setF("Width*0.66");

connection3.getY().getUfe().setF("Height*0");

shape1.getConnections().add(connection1);

shape1.getConnections().add(connection3);



// add connector shapes

Shape connector1 = new Shape();

Shape connector2 = new Shape();

Shape connector3 = new Shape();

long connecter1Id = diagram.addShape(connector1, connectorMaster, 0);

long connecter2Id = diagram.addShape(connector2, connectorMaster, 0);

long connecter3Id = diagram.addShape(connector3, connectorMaster, 0);

// connect shapes by index of conneecting points

page.connectShapesViaConnectorIndex(shape1.getID(), 6, shape2.getID(), 3, connecter1Id);

page.connectShapesViaConnectorIndex(shape1.getID(), 1, shape3.getID(), 3, connecter2Id);

page.connectShapesViaConnectorIndex(shape1.getID(), 7, shape4.getID(), 3, connecter3Id);

// save drawing

diagram.save("C:\\temp\\Drawing1_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
## **Rufen Sie die übergeordnete Form einer untergeordneten Form ab**
Aspose.Diagram for Java ermöglicht Entwicklern das Abrufen der übergeordneten Form einer Unterform.
### **Holen Sie sich die übergeordnete Form**
Die Klasse Shape bietet die Eigenschaft getParentShape zum Abrufen der übergeordneten Form.
#### **Holen Sie sich das Programmierbeispiel für übergeordnete Formen**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-RetrieveTheParentShape-RetrieveTheParentShape.java" >}}
