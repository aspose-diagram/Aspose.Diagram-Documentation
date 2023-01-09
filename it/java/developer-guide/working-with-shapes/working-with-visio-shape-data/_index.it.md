---
title: Utilizzo dei dati di forma Visio
type: docs
weight: 30
url: /it/java/working-with-visio-shape-data/
---
## **Aggiunta di una nuova forma in Visio**
Aspose.Diagram for Java consente di manipolare i diagrammi Microsoft Visio in diversi modi. Una delle cose che puoi fare è aggiungere nuove forme a un diagramma. Aspose.Diagram for Java consente di aggiungere una nuova forma a un diagram. La forma aggiunta può anche essere personalizzata utilizzando Aspose.Diagram for Java.

Questo argomento descrive come aggiungere una nuova forma rettangolare a un diagram.

Usa Aspose.Diagram for Java's API per creare nuove forme e quindi aggiungi queste forme a una raccolta di forme di diagram.

Per aggiungere una nuova forma:

1. **Trova la pagina** - Ogni Visio diagram contiene una raccolta di pagine. Gli sviluppatori possono recuperare l'ID o il nome pagina per pagina e memorizzare la pagina richiesta nel file[Pagina](https://reference.aspose.com/diagram//java/com.aspose.diagram/page)oggetto di classe.
1. **Aggiungi il Master di una forma richiesto** - Ogni Visio diagram contiene una raccolta di maestri. Gli sviluppatori possono aggiungere un master (per ID o nome) dal file stencil esistente (per percorso diretto o flusso di file).
1. **Aggiungi forma nel Visio diagram** - Gli sviluppatori possono inserire una nuova forma in Visio diagram per indice della pagina (a partire da 0), nome principale, PinX, PinY, altezza (opzionale) e larghezza (opzionale).
1. **Imposta le proprietà della forma** - Il metodo AddShape della classe Diagram restituisce l'ID della forma. Gli sviluppatori possono recuperare la forma da un Visio diagram utilizzando questo ID e quindi impostarne le proprietà, ad esempio colore, posizione, allineamento e testo.

|<p>**L'ingresso diagram** </p><p>![cose da fare:immagine_alt_testo](working-with-visio-shape-data_1.png)</p>|<p>**Lo diagram con una forma aggiunta** </p><p>![cose da fare:immagine_alt_testo](working-with-visio-shape-data_2.png)</p>|
|:- |:- |
### **Aggiungi esempio di programmazione**
Lo snippet di codice seguente mostra come eseguire ogni passaggio.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-AddingNewShape-AddingNewShape.java" >}}

{{% alert color="primary" %}}

 Accogliamo con favore le vostre domande e suggerimenti a[Aspose.Diagram Foro](https://forum.aspose.com/c/diagram/17). Ti risponderemo prontamente.

{{% /alert %}}
## **Recupero delle informazioni sulla forma**
[Lavorare con i diagrammi](/diagram/it/java/working-with-diagrams/)spiega come creare diagrammi, aggiungere forme e connettori, quindi come recuperare informazioni su diagram elementi come[pagine](/diagram/it/java/retrieve-get-copy-and-insert-a-page/), [maestri](/diagram/it/java/working-with-masters/) , connettori e[caratteri](/diagram/it/java/aspose-diagram-font-operations/). Questo articolo esamina come recuperare informazioni sulle forme in un diagram.

Ogni forma in uno diagram ha un ID e un nome. L'ID è importante quando si programma con Visio: è il metodo principale per accedere ad una forma. Ogni forma conserva anche informazioni su quale master (stencil) è composta.

 UN[Forma](https://reference.aspose.com/diagram//java/com.aspose.diagram/shape) è un oggetto in un disegno Visio. La proprietà Shapes, esposta dalla classe Page, supporta una raccolta di oggetti Aspose.Diagram.Shape. La proprietà Shapes può essere utilizzata per recuperare informazioni su una forma.

Nella finestra della console sottostante, ad esempio, è possibile visualizzare l'output delle informazioni per un diagram che conteneva quattro forme: due terminatori, un processo e un connettore dinamico. Ognuno ha un ID univoco e il nome della forma principale (stencil).

**Una finestra della console che mostra le informazioni sulla forma**

![cose da fare:immagine_alt_testo](working-with-visio-shape-data_3.png)

Per recuperare le informazioni sulla pagina Visio:

1. Carica un diagram.
1. Imposta un ciclo foreach per scorrere tutte le forme in diagram.
1. Visualizza le informazioni sulla forma.
### **Recupera esempio di programmazione**
Il seguente pezzo di codice recupera le informazioni sulla forma da un Visio diagram.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-RetrieveShapeInfo-RetrieveShapeInfo.java" >}}
## **Copia forme da un Visio esistente**
Aspose.Diagram for Java API consente agli sviluppatori di copiare le forme dalla pagina Visio di origine alla nuova pagina Visio diagram. Supporta anche la copia di forme di gruppo. Questo articolo descrive come copiare tutte le forme dalla pagina diagram di origine.

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
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-CopyShape-CopyShape.java" >}}

{{% alert color="primary" %}}

 Accogliamo con favore le vostre domande e suggerimenti a[Aspose.Diagram Foro](https://forum.aspose.com/c/diagram/17). Ti risponderemo prontamente.

{{% /alert %}}
## **Copia una forma Visio in un'altra istanza di forma**
Il metodo copy della classe Shape accetta un'istanza di forma da clonare.

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
## **Lettura dei dati di forma Visio**
 La raccolta Props esposta dalla classe Shape supporta il[Aspose.Diagram.Prop](https://reference.aspose.com/diagram//java/com.aspose.diagram/prop) oggetto. La proprietà può essere utilizzata per leggere i dati di una forma (proprietà personalizzate).
### **Leggi tutte le proprietà della forma**
Per identificare le proprietà personalizzate in Microsoft Visio:

1. In un diagram, fare clic con il pulsante destro del mouse su una forma.
1.  Selezionare**Dati** , poi**Dati di forma** dal menù.
 Tutte le proprietà esistenti sono elencate nella finestra di dialogo.

|**I dati di una forma, come si vede in Microsoft Visio.**|** |
|:- |:- |
|![cose da fare:immagine_alt_testo](http://i.imgur.com/2loM7b0.png)||


|**Una finestra della console che mostra l'output dei dati della forma.**|** |
|:- |:- |
|![cose da fare:immagine_alt_testo](http://i.imgur.com/kmAKNrx.png)||
#### **Leggi l'esempio di programmazione**
I frammenti di codice seguenti leggono i dati della forma (proprietà personalizzate).

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-ReadAllShapeProps-ReadAllShapeProps.java" >}}
### **Leggere una proprietà Shape per nome**
Il frammento di codice seguente legge una proprietà di forma per nome (proprietà personalizzata).
#### **Leggere per nome Esempio di programmazione**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-ReadShapePropByName-ReadShapePropByName.java" >}}
## **Usa gli indici di connessione per connettere le forme**
Aspose.Diagram for Java API consente già agli sviluppatori di aggiungere nuovi punti di connessione sulla forma e gli sviluppatori possono ora collegare le forme utilizzando gli indici di connessione.
### **Usa gli indici di connessione per connettere le forme**
Il membro connectShapesViaConnectorIndex esposto dalla classe Page può essere utilizzato per connettere forme mediante indici di connessione. Il codice seguente mostra come connettere le forme:

1. Inizializza un nuovo disegno.
1. Posiziona quattro forme rettangolari
1. Aggiungi due punti di connessione aggiuntivi, in modo che ci siano tre punti di connessione sulla linea di confine inferiore
1. Collega la prima forma da ciascuna connessione inferiore ad altre tre forme rettangolari dall'alto con connettori dinamici
1. Salva disegno
#### **Utilizzare gli indici di connessione per connettere le forme Esempio di programmazione**
Utilizzare il codice seguente nell'applicazione Java per connettere le forme utilizzando gli indici di connessione con Aspose.Diagram for Java API.

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
## **Recupera la forma padre di una forma secondaria**
Aspose.Diagram for Java consente agli sviluppatori di recuperare la forma padre di una forma secondaria.
### **Ottieni la forma genitore**
La classe Shape offre la proprietà getParentShape per recuperare la forma genitore.
#### **Ottieni l'esempio di programmazione della forma genitore**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-RetrieveTheParentShape-RetrieveTheParentShape.java" >}}
