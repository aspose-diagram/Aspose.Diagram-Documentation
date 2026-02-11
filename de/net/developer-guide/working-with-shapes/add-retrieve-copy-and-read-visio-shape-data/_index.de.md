---
title: Visio-Shape-Daten hinzufügen, abrufen, kopieren und lesen
type: docs
weight: 10
url: /de/net/add-retrieve-copy-and-read-visio-shape-data/
description: In diesem Abschnitt wird erläutert, wie Sie eine Form hinzufügen, die Eigenschaften einer Form festlegen oder eine Form mit Aspose.Diagram kopieren.
---
## **Hinzufügen einer neuen Form in Visio**
Mit Aspose.Diagram for .NET können Sie Microsoft Visio Diagramme auf verschiedene Weise bearbeiten. Eines der Dinge, die Sie tun können, ist das Hinzufügen neuer Formen zu einem Diagramm. Mit Aspose.Diagram for .NET können Sie einer diagram eine neue Form hinzufügen. Die hinzugefügte Form kann auch mit Aspose.Diagram for .NET angepasst werden.

In diesem Thema wird beschrieben, wie Sie einer diagram eine neue rechteckige Form hinzufügen.

Verwenden Sie Aspose.Diagram for .NET API, um neue Formen zu erstellen, und fügen Sie diese Formen dann der Formensammlung von diagram hinzu.

So fügen Sie eine neue Form hinzu:

1. **Finde die Seite** - Jede Visio diagram enthält eine Sammlung von Seiten. Entwickler können die Seite nach Seiten-ID oder Name abrufen und die erforderliche Seite in der speichern[Buchseite](http://www.aspose.com/api/net/diagram/aspose.diagram/page)Klasse Objekt.
1. **Fügen Sie den erforderlichen Master einer Form hinzu** - Jeder Visio diagram enthält eine Sammlung von Meistern. Entwickler können einen Master (nach ID oder Name) aus der vorhandenen Schablonendatei (über direkten Pfad oder Dateistream) hinzufügen.
1. **Fügen Sie Form in Visio diagram hinzu** - Entwickler können eine neue Form im Visio diagram nach Seitenindex (beginnend bei 0), Hauptname, PinX, PinY, Höhe (optional) und Breite (optional) platzieren.
1. **Formeigenschaften festlegen** - AddShape-Methode der Klasse Diagram gibt die Shape-ID zurück. Entwickler können die Form von Visio diagram abrufen, indem sie diese ID verwenden, und dann ihre Eigenschaften festlegen, z. B. Farbe, Position, Ausrichtung und Text.

|<p>**Die Eingabe diagram** </p><p>![todo: Bild_alt_Text](add-retrieve-copy-and-read-visio-shape-data_1.png)</p>|<p>**Die diagram mit einer hinzugefügten Form** </p><p>![todo: Bild_alt_Text](add-retrieve-copy-and-read-visio-shape-data_2.png)</p>|
|:- |:- |
### **Programmierbeispiel hinzufügen**
Das folgende Code-Snippet zeigt, wie die einzelnen Schritte ausgeführt werden.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-2");

// Add master with stencil file path and master name
string masterName = "Rectangle";
diagram.AddMaster(dataDir + "Basic Shapes.vss", masterName);
            
// Page indexing starts from 0
int PageIndex = 1;
double width = 2, height = 2, pinX = 4.25, pinY = 4.5;
// Add a new rectangle shape
long rectangleId = diagram.AddShape(pinX, pinY, width, height, masterName, PageIndex);
            
// Set shape properties 
Shape rectangle = page.Shapes.GetShape(rectangleId);
rectangle.XForm.PinX.Value = 5;
rectangle.XForm.PinY.Value = 5;
rectangle.Type = TypeValue.Shape;
rectangle.Text.Value.Add(new Txt("Aspose Diagram"));
rectangle.TextStyle = diagram.StyleSheets[3];
rectangle.Line.LineColor.Value = "#ff0000";
rectangle.Line.LineWeight.Value = 0.03;
rectangle.Line.Rounding.Value = 0.1;
rectangle.Fill.FillBkgnd.Value = "#ff00ff";
rectangle.Fill.FillForegnd.Value = "#ebf8df";

diagram.Save(dataDir + "AddShape_out.vsdx", SaveFileFormat.VSDX);
Console.WriteLine("Shape has been added.");

{{< /highlight >}}


{{% alert color="primary" %}}

 Wir freuen uns über Ihre Fragen und Anregungen unter[Aspose.Diagram Forum](https://forum.aspose.com/c/diagram/17). Wir antworten umgehend.

{{% /alert %}}
## **Forminformationen abrufen**
[Arbeiten mit Diagrammen](/diagram/de/net/working-with-diagrams/)erklärt, wie man Diagramme erstellt, Formen und Verbinder hinzufügt und dann Informationen über diagram-Elemente wie z[Seiten](/diagram/de/net/retrieve-2c-get-2c-copy-and-insert-a-page/), [Meister](https://docs.aspose.com/diagram/net/working-with-masters/), [Anschlüsse](/diagram/de/net/retrieving-connector-information/) und[Schriftarten](/diagram/de/net/retrieving-font-information/). In diesem Artikel wird beschrieben, wie Sie Informationen zu Formen in einem diagram abrufen.

Jede Form in einem diagram hat eine ID und einen Namen. Die ID ist beim Programmieren mit Visio wichtig: Sie ist die Hauptmethode für den Zugriff auf eine Form. Jede Form enthält auch Informationen darüber, aus welchem Master (Schablone) sie besteht.

 EIN[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) ist ein Objekt in einer Visio-Zeichnung. Die Shapes-Eigenschaft, die von der Page-Klasse verfügbar gemacht wird, unterstützt eine Sammlung von Aspose.Diagram.Shape-Objekten. Die Shapes-Eigenschaft kann verwendet werden, um Informationen zu einer Form abzurufen.

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


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load diagram
Diagram vsdDiagram = new Diagram(dataDir + "RetrieveShapeInfo.vsd");

foreach (Aspose.Diagram.Shape shape in vsdDiagram.Pages[0].Shapes)
{
    // Display information about the shapes
    Console.WriteLine("\nShape ID : " + shape.ID);
    Console.WriteLine("Name : " + shape.Name);
    Console.WriteLine("Master Shape : " + shape.Master.Name);
}

{{< /highlight >}}

## **Kopieren Sie Formen von einem vorhandenen Visio**
Aspose.Diagram for .NET API ermöglicht es Entwicklern, Formen von der Quellseite Visio auf die neue Seite Visio diagram zu kopieren. Es unterstützt auch das Kopieren von Gruppenformen. Dieser Artikel beschreibt, wie Sie alle Shapes von der Quellseite diagram kopieren.

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

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();
            
// Load a source Visio
Diagram srcVisio = new Diagram(dataDir + "Drawing1.vsdx");
            
// Initialize a new Visio
Diagram newDiagram = new Diagram();

// Add all masters from the source Visio diagram
MasterCollection originalMasters = srcVisio.Masters;
foreach (Master master in originalMasters)
    newDiagram.AddMaster(srcVisio, master.Name);

// Get the page object from the original diagram
Aspose.Diagram.Page SrcPage = srcVisio.Pages.GetPage("Page-1");
// Copy themes from the source diagram
newDiagram.CopyTheme(srcVisio);
// Copy pagesheet of the source Visio page
newDiagram.Pages[0].PageSheet.Copy(SrcPage.PageSheet);

// Copy shapes from the source Visio page
foreach (Aspose.Diagram.Shape shape in SrcPage.Shapes)
{
    newDiagram.Pages[0].Shapes.Add(shape);
}
// Save the new Visio
newDiagram.Save(dataDir + "CopyShapes_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


{{% alert color="primary" %}}

 Wir freuen uns über Ihre Fragen und Anregungen unter[Aspose.Diagram Forum](https://forum.aspose.com/c/diagram/17). Wir antworten umgehend.

{{% /alert %}}
## **Kopieren Sie eine Visio-Form in eine andere Forminstanz**
Die Copy-Methode der Shape-Klasse nimmt eine Shape-Instanz zum Klonen.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Shape newShape = new Shape();

// copy diagram

newShape.Copy(diagram.Pages[0].Shapes[0]);

newShape.ID = 3;

newShape.XForm.PinX.Value = 1;

newShape.XForm.PinY.Value = 1;

{{< /highlight >}}
## **Lesen von Visio Formdaten**
 Die Props-Sammlung, die von der bereitgestellt wird[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Klasse unterstützt die[Aspose.Diagram.Prop](http://www.aspose.com/api/net/diagram/aspose.diagram/prop) Objekt. Die Eigenschaft kann verwendet werden, um die Daten einer Form (benutzerdefinierte Eigenschaften) zu lesen.
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


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

foreach (Aspose.Diagram.Shape shape in page.Shapes)
{
    if (shape.Name == "Process1")
    {
        foreach (Prop property in shape.Props)
        {
            Console.WriteLine(property.Label.Value + ": " + property.Value.Val);
        }
        break;
    }
}

{{< /highlight >}}

### **Lesen Sie eine Shape-Eigenschaft nach Namen**
Das folgende Code-Snippet liest eine Shape-Eigenschaft nach Namen (benutzerdefinierte Eigenschaft).
#### **Read by Name Programmierbeispiel**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

foreach (Aspose.Diagram.Shape shape in page.Shapes)
{
    if (shape.Name == "Process1")
    {
        Prop property = shape.Props.GetProp("Name1");
        Console.WriteLine(property.Label.Value + ": " + property.Value.Val);
    }
}

{{< /highlight >}}

### **Lesen Sie VererbenProps of Shape**
Das Code-Snippet unten liest InheritProps einer Form.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

foreach (Aspose.Diagram.Shape shape in page.Shapes)
{
    foreach (Aspose.Diagram.Prop prop in shape.InheritProps)
    {
        Console.WriteLine(prop.Name);
        Console.WriteLine(prop.Label.Value);
        Console.WriteLine(prop.Prompt.Value);
        Console.WriteLine(prop.Type.Value.ToString());
        Console.WriteLine(prop.Value.Val);
        Console.WriteLine(prop.Format.Value);
    }
}

{{< /highlight >}}

## **Visio Formen hinzufügen und verbinden**
 Aspose.Diagram for .NET ermöglicht es Ihnen, benutzerdefinierte Formen hinzuzufügen und zu verbinden[Diagramme, die Sie erstellen](https://products.aspose.com/diagram/net/).
### **Formen hinzufügen und verbinden**
Der Code in den folgenden Beispielen zeigt, wie Sie:

1. Erstellen Sie eine diagram.
1. Fügen Sie Formen hinzu und passen Sie sie an (Rechteck, Stern, Sechseck).
1. Verbinden Sie die Stern- und Sechseckformen mit dem Rechteck.
1. Speichern Sie die diagram.
#### **Formen hinzufügen und verbinden Programmierbeispiel**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_TechnicalArticles();

// Set license (you can add 10 shapes without setting a license)
// License lic = new License();
// Lic.SetLicense(dataDir + "Aspose.Total.lic");

// Load masters from any existing diagram, stencil or template
// And add in the new diagram
string visioStencil = dataDir + "AddConnectShapes.vss";

// Names of the masters present in the stencil
string rectangleMaster = @"Rectangle", starMaster = @"Star 7",
    hexagonMaster = @"Hexagon", connectorMaster = "Dynamic connector";

int pageNumber = 0;
double width = 2, height = 2, pinX = 4.25, pinY = 9.5;

// Create a new diagram
Diagram diagram = new Diagram(visioStencil);

// Add a new rectangle shape
long rectangleId = diagram.AddShape(
    pinX, pinY, width, height, rectangleMaster, pageNumber);

// Set the new shape's properties
Shape shape = diagram.Pages[pageNumber].Shapes.GetShape(rectangleId);
shape.Text.Value.Add(new Txt(@"Rectangle text."));
shape.Name = "Rectangle1";
shape.XForm.LocPinX.Ufe.F = "Width*0.5";
shape.XForm.LocPinY.Ufe.F = "Height*0.5";
shape.Line.LineColor.Value = "7";
shape.Line.LineWeight.Value = 0.03;
shape.Fill.FillBkgnd.Value = "1";
shape.Fill.FillForegnd.Value = "3";
shape.Fill.FillPattern.Value = 31;

// Add a new star shape
pinX = 2.0;
pinY = 4.5;
long starId = diagram.AddShape(
    pinX, pinY, width, height, starMaster, pageNumber);

// Set the star shape's properties
shape = diagram.Pages[pageNumber].Shapes.GetShape(starId);
shape.Text.Value.Add(new Txt(@"Star text."));
shape.Name = "Star1";
shape.XForm.LocPinX.Ufe.F = "Width*0.5";
shape.XForm.LocPinY.Ufe.F = "Height*0.5";
shape.Line.LineColor.Value = "#ff0000";
shape.Line.LineWeight.Value = 0.03;
shape.Fill.FillBkgnd.Value = "#ff00ff";
shape.Fill.FillForegnd.Value = "#0000ff";
shape.Fill.FillPattern.Value = 31;

// Add a new hexagon shape
pinX = 7.0;
long hexagonId = diagram.AddShape(
    pinX, pinY, width, height, hexagonMaster, pageNumber);

// Set the hexagon shape's properties
shape = diagram.Pages[pageNumber].Shapes.GetShape(hexagonId);
shape.Text.Value.Add(new Txt(@"Hexagon text."));
shape.Name = "Hexagon1";
shape.XForm.LocPinX.Ufe.F = "Width*0.5";
shape.XForm.LocPinY.Ufe.F = "Height*0.5";
shape.Line.LineWeight.Value = 0.03;
shape.Fill.FillPattern.Value = 31;

// Add master to dynamic connector from the stencil
diagram.AddMaster(visioStencil, connectorMaster);

// Connect rectangle and star shapes
Shape connector1 = new Shape();
long connecter1Id = diagram.AddShape(connector1, connectorMaster, 0);
diagram.Pages[0].ConnectShapesViaConnector(rectangleId, ConnectionPointPlace.Bottom,
    starId, ConnectionPointPlace.Top, connecter1Id);

// Connect rectangle and hexagon shapes
Shape connector2 = new Shape();
long connecter2Id = diagram.AddShape(connector2, connectorMaster, 0);
diagram.Pages[0].ConnectShapesViaConnector(rectangleId, ConnectionPointPlace.Bottom,
    hexagonId, ConnectionPointPlace.Left, connecter2Id);

// Save the diagram
diagram.Save(dataDir + "AddConnectShapes_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Verwenden Sie Verbindungsindizes, um Shapes zu verbinden**
Aspose.Diagram for .NET API ermöglicht es Entwicklern bereits, neue Verbindungspunkte auf der Form hinzuzufügen, und Entwickler können jetzt Formen mithilfe von Verbindungsindizes verbinden.
### **Verwenden Sie Verbindungsindizes, um Shapes zu verbinden**
Das ConnectShapesViaConnectorIndex-Member, das von verfügbar gemacht wird[Buchseite](https://reference.aspose.com/diagram/net/aspose.diagram/page)-Klasse kann verwendet werden, um Shapes mithilfe von Verbindungsindizes zu verbinden. Der folgende Code zeigt, wie Shapes verbunden werden:

1. Initialisieren Sie eine neue Zeichnung.
1. Platziere vier rechteckige Formen
1. Fügen Sie zwei zusätzliche Verbindungspunkte hinzu, sodass sich auf der unteren Begrenzungslinie drei Verbindungspunkte befinden würden
1. Verbinden Sie die erste Form von jeder unteren Verbindung mit anderen drei rechteckigen Formen von oben mit dynamischen Verbindern
1. Zeichnung speichern
#### **Verwenden Sie Verbindungsindizes, um Shapes zu verbinden Programmierbeispiel**
Verwenden Sie den folgenden Code in Ihrer .NET-Anwendung, um Shapes mithilfe von Verbindungsindizes mit Aspose.Diagram for .NET API zu verbinden.

**C#**

{{< highlight "java" >}}

 // initialize a new drawing

Diagram diagram = new Diagram();

// get page by index

Aspose.Diagram.Page page = diagram.Pages[0];

// add masters

string connectorMaster = "Dynamic connector", rectangle = "Rectangle";

int pageNumber = 0;

double width = 2, height = 2, pinX = 4.25, pinY = 9.5;

diagram.AddMaster(@"C:\temp\Basic Shapes.vss", rectangle);

diagram.AddMaster(@"C:\temp\Basic Shapes.vss", connectorMaster);

// add shapes

long shape1_ID = diagram.AddShape(4.5, 7, rectangle, pageNumber);

long shape2_ID = diagram.AddShape(2.25, 4.5, rectangle, pageNumber);

long shape3_ID = diagram.AddShape(4.5, 4.5, rectangle, pageNumber);

long shape4_ID = diagram.AddShape(6.75, 4.5, rectangle, pageNumber);

// get shapes by ID

Aspose.Diagram.Shape shape1 = page.Shapes.GetShape(shape1_ID);

Aspose.Diagram.Shape shape2 = page.Shapes.GetShape(shape2_ID);

Aspose.Diagram.Shape shape3 = page.Shapes.GetShape(shape3_ID);

Aspose.Diagram.Shape shape4 = page.Shapes.GetShape(shape4_ID);

// add two more connection points

Connection connection1 = new Connection();

connection1.X.Ufe.F = "Width*0.33";

connection1.Y.Ufe.F = "Height*0";

Connection connection3 = new Connection();

connection3.X.Ufe.F = "Width*0.66";

connection3.Y.Ufe.F = "Height*0";

shape1.Connections.Add(connection1);

shape1.Connections.Add(connection3);



// add connector shapes

Aspose.Diagram.Shape connector1 = new Aspose.Diagram.Shape();

Aspose.Diagram.Shape connector2 = new Aspose.Diagram.Shape();

Aspose.Diagram.Shape connector3 = new Aspose.Diagram.Shape();

long connecter1Id = diagram.AddShape(connector1, connectorMaster, 0);

long connecter2Id = diagram.AddShape(connector2, connectorMaster, 0);

long connecter3Id = diagram.AddShape(connector3, connectorMaster, 0);

// connect shapes by index of conneecting points

page.ConnectShapesViaConnectorIndex(shape1.ID, 6, shape2.ID, 3, connecter1Id);

page.ConnectShapesViaConnectorIndex(shape1.ID, 1, shape3.ID, 3, connecter2Id);

page.ConnectShapesViaConnectorIndex(shape1.ID, 7, shape4.ID, 3, connecter3Id);

// save drawing

diagram.Save(@"C:\temp\Drawing1_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
## **Rufen Sie die übergeordnete Form einer untergeordneten Form ab**
Aspose.Diagram for .NET ermöglicht Entwicklern das Abrufen der übergeordneten Form einer Unterform.
### **Holen Sie sich die übergeordnete Form**
Das[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)Die Klasse bietet die ParentShape-Eigenschaft zum Abrufen der übergeordneten Form.
#### **Holen Sie sich das Programmierbeispiel für übergeordnete Formen**

{{< highlight csharp >}}
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();
// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a sub-shape by page name, group shape ID, and then sub-shape ID
Shape shape = diagram.Pages.GetPage("Page-3").Shapes.GetShape(13).Shapes.GetShape(2);
Shape parentShape = shape.ParentShape;
Console.WriteLine("Parent Shape's Properties:");
Console.WriteLine("Shape ID: " + parentShape.ID);
Console.WriteLine("Shape Name: " + parentShape.Name);
Console.WriteLine("Shape Type: " + parentShape.Type);
{{< /highlight >}}

