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

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-AddingNewShape-AddingNewShape.cs" >}}

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

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-RetrieveShapeInfo-RetrieveShapeInfo.cs" >}}
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
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-CopyShape-CopyShape.cs" >}}

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

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-ReadAllShapeProps-ReadAllShapeProps.cs" >}}
### **Leggere una proprietà Shape per nome**
Il frammento di codice seguente legge una proprietà di forma per nome (proprietà personalizzata).
#### **Leggere per nome Esempio di programmazione**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-ReadShapePropByName-ReadShapePropByName.cs" >}}
### **Leggi InheritProps of Shape**
Il frammento di codice seguente legge InheritProps di una forma.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-InheritProps-InheritProps.cs" >}}
## **Aggiungi e collega Visio Forme**
 Aspose.Diagram for .NET consente di aggiungere forme personalizzate e collegarle in[diagrammi che crei](https://products.aspose.com/diagram/net/).
### **Aggiunta e connessione di forme**
Il codice negli esempi seguenti mostra come:

1. Crea uno diagram.
1. Aggiungi e personalizza forme (rettangolo, stella, esagono).
1. Collega le forme stella ed esagono al rettangolo.
1. Salva lo diagram.
#### **Esempio di programmazione di aggiunta e connessione di forme**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Technical-Articles-AddConnectShapes-AddConnectShapes.cs" >}}
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
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-RetrieveTheParentShape-RetrieveTheParentShape.cs" >}}
