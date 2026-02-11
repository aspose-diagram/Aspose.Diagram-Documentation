---
title: Aggiungi, recupera, copia e leggi Visio Shape Data
type: docs
weight: 10
url: /it/net/add-retrieve-copy-and-read-visio-shape-data/
description: Questa sezione spiega come aggiungere una forma, impostare la proprietà della forma o copiare una forma con Aspose.Diagram.
---
## **Aggiunta di una nuova forma in Visio**
Aspose.Diagram for .NET consente di manipolare i diagrammi Microsoft Visio in diversi modi. Una delle cose che puoi fare è aggiungere nuove forme a un diagramma. Aspose.Diagram for .NET consente di aggiungere una nuova forma a un diagram. La forma aggiunta può anche essere personalizzata utilizzando Aspose.Diagram for .NET.

Questo argomento descrive come aggiungere una nuova forma rettangolare a un diagram.

Utilizzare Aspose.Diagram for .NET API per creare nuove forme e quindi aggiungere queste forme a una raccolta di forme di diagram.

Per aggiungere una nuova forma:

1. **Trova la pagina** - Ogni Visio diagram contiene una raccolta di pagine. Gli sviluppatori possono recuperare l'ID o il nome pagina per pagina e memorizzare la pagina richiesta nel file[Pagina](http://www.aspose.com/api/net/diagram/aspose.diagram/page)oggetto di classe.
1. **Aggiungi il Master di una forma richiesto** - Ogni Visio diagram contiene una raccolta di maestri. Gli sviluppatori possono aggiungere un master (per ID o nome) dal file stencil esistente (per percorso diretto o flusso di file).
1. **Aggiungi forma nel Visio diagram** - Gli sviluppatori possono inserire una nuova forma in Visio diagram per indice della pagina (a partire da 0), nome principale, PinX, PinY, altezza (opzionale) e larghezza (opzionale).
1. **Imposta le proprietà della forma** - Il metodo AddShape della classe Diagram restituisce l'ID della forma. Gli sviluppatori possono recuperare la forma da un Visio diagram utilizzando questo ID e quindi impostarne le proprietà, ad esempio colore, posizione, allineamento e testo.

|<p>**L'ingresso diagram** </p><p>![cose da fare:immagine_alt_testo](add-retrieve-copy-and-read-visio-shape-data_1.png)</p>|<p>**Lo diagram con una forma aggiunta** </p><p>![cose da fare:immagine_alt_testo](add-retrieve-copy-and-read-visio-shape-data_2.png)</p>|
|:- |:- |
### **Aggiungi esempio di programmazione**
Lo snippet di codice seguente mostra come eseguire ogni passaggio.

```
{{< highlight "csharp" >}}
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
```

{{% alert color="primary" %}}

 Accogliamo con favore le vostre domande e suggerimenti a[Aspose.Diagram Foro](https://forum.aspose.com/c/diagram/17). Ti risponderemo prontamente.

{{% /alert %}}
## **Recupero delle informazioni sulla forma**
[Lavorare con i diagrammi](/diagram/it/net/working-with-diagrams/)spiega come creare diagrammi, aggiungere forme e connettori, quindi come recuperare informazioni su diagram elementi come[pagine](/diagram/it/net/retrieve-2c-get-2c-copy-and-insert-a-page/), [maestri](https://docs.aspose.com/diagram/net/working-with-masters/), [connettori](/diagram/it/net/retrieving-connector-information/) e[caratteri](/diagram/it/net/retrieving-font-information/). Questo articolo esamina come recuperare informazioni sulle forme in un diagram.

Ogni forma in uno diagram ha un ID e un nome. L'ID è importante quando si programma con Visio: è il metodo principale per accedere ad una forma. Ogni forma conserva anche informazioni su quale master (stencil) è composta.

 UN[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) è un oggetto in un disegno Visio. La proprietà Shapes, esposta dalla classe Page, supporta una raccolta di oggetti Aspose.Diagram.Shape. La proprietà Shapes può essere utilizzata per recuperare informazioni su una forma.

Nella finestra della console sottostante, ad esempio, è possibile visualizzare l'output delle informazioni per un diagram che conteneva quattro forme: due terminatori, un processo e un connettore dinamico. Ognuno ha un ID univoco e il nome della forma principale (stencil).

|**Una finestra della console che mostra le informazioni sulla forma**|
|:- |
|![cose da fare:immagine_alt_testo](add-retrieve-copy-and-read-visio-shape-data_3.png)|
Per recuperare le informazioni sulla pagina Visio:

1. Carica un diagram.
1. Imposta un ciclo foreach per scorrere tutte le forme in diagram.
1. Visualizza le informazioni sulla forma.
### **Recupera esempio di programmazione**
Il seguente pezzo di codice recupera le informazioni sulla forma da un Visio diagram.

```
{{< highlight "csharp" >}}
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
```
## **Copia forme da un Visio esistente**
Aspose.Diagram for .NET API consente agli sviluppatori di copiare le forme dalla pagina Visio di origine alla nuova pagina Visio diagram. Supporta anche la copia di forme di gruppo. Questo articolo descrive come copiare tutte le forme dalla pagina diagram di origine.

Per copiare le forme, gli sviluppatori devono anche copiare i temi PageSheet e Visio di origine per conservare lo stile di riempimento delle forme e altre proprietà di formattazione.

Questo esempio funziona come segue:

1. Carica una fonte Visio.
1. Inizializza un nuovo Visio
1. Aggiungi master e temi dalla fonte Visio.
1. Ottieni la pagina dalla fonte Visio.
1. Copia il suo foglio di pagina nella nuova pagina Visio.
1. Scorri le forme della pagina Visio di origine.
1. Imposta il suo nuovo ID e aggiungilo alla nuova pagina Visio.
1. Salva il nuovo Visio nella memoria locale.
### **Copia esempio di programmazione**
```
{{< highlight "csharp" >}}
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
```

{{% alert color="primary" %}}

 Accogliamo con favore le vostre domande e suggerimenti a[Aspose.Diagram Foro](https://forum.aspose.com/c/diagram/17). Ti risponderemo prontamente.

{{% /alert %}}
## **Copia una forma Visio in un'altra istanza di forma**
Il metodo Copy della classe Shape accetta un'istanza di forma da clonare.

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
## **Lettura dei dati di forma Visio**
 La collezione Props esposta dal[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) la classe supporta il[Aspose.Diagram.Prop](http://www.aspose.com/api/net/diagram/aspose.diagram/prop) oggetto. La proprietà può essere utilizzata per leggere i dati di una forma (proprietà personalizzate).
### **Leggi tutte le proprietà della forma**
Per identificare le proprietà personalizzate in Microsoft Visio:

1. In un diagram, fare clic con il pulsante destro del mouse su una forma.
1.  Selezionare**Dati** , poi**Dati di forma** dal menù.
 Tutte le proprietà esistenti sono elencate nella finestra di dialogo.

|**I dati di una forma, come si vede in Microsoft Visio.**|** |
|:- |:- |
|![cose da fare:immagine_alt_testo](add-retrieve-copy-and-read-visio-shape-data_4.png)||


|**Una finestra della console che mostra l'output dei dati della forma.**|** |
|:- |:- |
|![cose da fare:immagine_alt_testo](add-retrieve-copy-and-read-visio-shape-data_5.png)||
#### **Leggi l'esempio di programmazione**
I frammenti di codice seguenti leggono i dati della forma (proprietà personalizzate).

```
{{< highlight "csharp" >}}
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
```
### **Leggere una proprietà Shape per nome**
Il frammento di codice seguente legge una proprietà di forma per nome (proprietà personalizzata).
#### **Leggere per nome Esempio di programmazione**
```
{{< highlight "csharp" >}}
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
```
### **Leggi InheritProps of Shape**
Il frammento di codice seguente legge InheritProps di una forma.

```
{{< highlight "csharp" >}}
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
```
## **Aggiungi e collega Visio Forme**
 Aspose.Diagram for .NET consente di aggiungere forme personalizzate e collegarle in[diagrammi che crei](https://products.aspose.com/diagram/net/).
### **Aggiunta e connessione di forme**
Il codice negli esempi seguenti mostra come:

1. Crea uno diagram.
1. Aggiungi e personalizza forme (rettangolo, stella, esagono).
1. Collega le forme stella ed esagono al rettangolo.
1. Salva lo diagram.
#### **Esempio di programmazione di aggiunta e connessione di forme**
```
{{< highlight "csharp" >}}
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
```
## **Usa gli indici di connessione per connettere le forme**
Aspose.Diagram for .NET API consente già agli sviluppatori di aggiungere nuovi punti di connessione sulla forma e gli sviluppatori possono ora collegare le forme utilizzando gli indici di connessione.
### **Usa gli indici di connessione per connettere le forme**
Il membro ConnectShapesViaConnectorIndex esposto da[Pagina](https://reference.aspose.com/diagram/net/aspose.diagram/page)class può essere utilizzata per connettere forme utilizzando gli indici di connessione. Il codice seguente mostra come connettere le forme:

1. Inizializza un nuovo disegno.
1. Posiziona quattro forme rettangolari
1. Aggiungi due punti di connessione aggiuntivi, in modo che ci siano tre punti di connessione sulla linea di confine inferiore
1. Collega la prima forma da ciascuna connessione inferiore ad altre tre forme rettangolari dall'alto con connettori dinamici
1. Salva disegno
#### **Utilizzare gli indici di connessione per connettere le forme Esempio di programmazione**
Utilizzare il codice seguente nell'applicazione .NET per connettere le forme utilizzando gli indici di connessione con Aspose.Diagram for .NET API.

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
## **Recupera la forma padre di una forma secondaria**
Aspose.Diagram for .NET consente agli sviluppatori di recuperare la forma padre di una forma secondaria.
### **Ottieni la forma genitore**
Il[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)class offre la proprietà ParentShape per recuperare la forma genitore.
#### **Ottieni l'esempio di programmazione della forma genitore**
```
{{< highlight "csharp" >}}
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
```
