---
title: Aggiungi, recupera, copia e leggi Visio Shape Data
type: docs
weight: 10
url: /it/java/add-retrieve-copy-and-read-visio-shape-data/
description: Questa sezione spiega come aggiungere una forma, impostare la proprietà della forma o copiare una forma con Aspose.Diagram.
---
## **Aggiunta di una nuova forma in Visio**
Aspose.Diagram for Java consente di manipolare i diagrammi Microsoft Visio in diversi modi. Una delle cose che puoi fare è aggiungere nuove forme a un diagramma. Aspose.Diagram for Java consente di aggiungere una nuova forma a un diagram. La forma aggiunta può anche essere personalizzata utilizzando Aspose.Diagram for Java.

Questo argomento descrive come aggiungere una nuova forma rettangolare a un diagram.

Utilizzare Aspose.Diagram for Java API per creare nuove forme e quindi aggiungere queste forme a una raccolta di forme di diagram.

Per aggiungere una nuova forma:

1. **Trova la pagina** - Ogni Visio diagram contiene una raccolta di pagine. Gli sviluppatori possono recuperare l'ID o il nome pagina per pagina e memorizzare la pagina richiesta nel file[Pagina](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)oggetto di classe.
1. **Aggiungi il Master di una forma richiesto** - Ogni Visio diagram contiene una raccolta di maestri. Gli sviluppatori possono aggiungere un master (per ID o nome) dal file stencil esistente (per percorso diretto o flusso di file).
1. **Aggiungi forma nel Visio diagram** - Gli sviluppatori possono inserire una nuova forma in Visio diagram per indice della pagina (a partire da 0), nome principale, PinX, PinY, altezza (opzionale) e larghezza (opzionale).
1. **Imposta le proprietà della forma** - Il metodo AddShape della classe Diagram restituisce l'ID della forma. Gli sviluppatori possono recuperare la forma da un Visio diagram utilizzando questo ID e quindi impostarne le proprietà, ad esempio colore, posizione, allineamento e testo.

|<p>**L'ingresso diagram** </p><p>![cose da fare:immagine_alt_testo](add-retrieve-copy-and-read-visio-shape-data_1.png)</p>|<p>**Lo diagram con una forma aggiunta** </p><p>![cose da fare:immagine_alt_testo](add-retrieve-copy-and-read-visio-shape-data_2.png)</p>|
|:- |:- |
### **Aggiungi esempio di programmazione**
Lo snippet di codice seguente mostra come eseguire ogni passaggio.

```
{{< highlight "java" >}}
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
```

{{% alert color="primary" %}}

 Accogliamo con favore le vostre domande e suggerimenti a[Aspose.Diagram Foro](https://forum.aspose.com/c/diagram/17). Ti risponderemo prontamente.

{{% /alert %}}
## **Recupero delle informazioni sulla forma**
[Lavorare con i diagrammi](/diagram/it/java/working-with-diagrams/)spiega come creare diagrammi, aggiungere forme e connettori, quindi come recuperare informazioni su diagram elementi come[pagine](/diagram/it/java/retrieve-get-copy-and-insert-a-page/), [maestri](https://docs.aspose.com/diagram/java/working-with-masters/), [connettori](https://reference.aspose.com/diagram/java/com.aspose.diagram/ConnectCollection) e[caratteri](https://reference.aspose.com/diagram/java/com.aspose.diagram/FontCollection). Questo articolo esamina come recuperare informazioni sulle forme in un diagram.

Ogni forma in uno diagram ha un ID e un nome. L'ID è importante quando si programma con Visio: è il metodo principale per accedere ad una forma. Ogni forma conserva anche informazioni su quale master (stencil) è composta.

 UN[Forma](http://www.aspose.com/api/java/diagram/com.aspose.diagram/shape) è un oggetto in un disegno Visio. La proprietà Shapes, esposta dalla classe Page, supporta una raccolta di oggetti Aspose.Diagram.Shape. La proprietà Shapes può essere utilizzata per recuperare informazioni su una forma.

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
{{< highlight "java" >}}
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
```

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
```
{{< highlight "java" >}}
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
```


{{% alert color="primary" %}}

 Accogliamo con favore le vostre domande e suggerimenti a[Aspose.Diagram Foro](https://forum.aspose.com/c/diagram/17). Ti risponderemo prontamente.

{{% /alert %}}
## **Copia una forma Visio in un'altra istanza di forma**
Il metodo Copy della classe Shape accetta un'istanza di forma da clonare.

## **Lettura dei dati di forma Visio**
 La collezione Props esposta dal[Forma](http://www.aspose.com/api/java/diagram/com.aspose.diagram/shape) la classe supporta il[Aspose.Diagram.Prop](http://www.aspose.com/api/java/diagram/com.aspose.diagram/prop) oggetto. La proprietà può essere utilizzata per leggere i dati di una forma (proprietà personalizzate).
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
{{< highlight "java" >}}
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
```

### **Leggere una proprietà Shape per nome**
Il frammento di codice seguente legge una proprietà di forma per nome (proprietà personalizzata).
#### **Leggere per nome Esempio di programmazione**
```
{{< highlight "java" >}}
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
```

## **Usa gli indici di connessione per connettere le forme**
Aspose.Diagram for Java API consente già agli sviluppatori di aggiungere nuovi punti di connessione sulla forma e gli sviluppatori possono ora collegare le forme utilizzando gli indici di connessione.
### **Usa gli indici di connessione per connettere le forme**
Il membro ConnectShapesViaConnectorIndex esposto da[Pagina](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)class può essere utilizzata per connettere forme utilizzando gli indici di connessione.

1. Inizializza un nuovo disegno.
1. Posiziona quattro forme rettangolari
1. Aggiungi due punti di connessione aggiuntivi, in modo che ci siano tre punti di connessione sulla linea di confine inferiore
1. Collega la prima forma da ciascuna connessione inferiore ad altre tre forme rettangolari dall'alto con connettori dinamici
1. Salva disegno
#### **Utilizzare gli indici di connessione per connettere le forme Esempio di programmazione**
Utilizzare il codice seguente nell'applicazione Java per connettere le forme utilizzando gli indici di connessione con Aspose.Diagram for Java API.

## **Recupera la forma padre di una forma secondaria**
Aspose.Diagram for Java consente agli sviluppatori di recuperare la forma padre di una forma secondaria.
### **Ottieni la forma genitore**
Il[Forma](http://www.aspose.com/api/java/diagram/com.aspose.diagram/shape)class offre la proprietà ParentShape per recuperare la forma genitore.
#### **Ottieni l'esempio di programmazione della forma genitore**
```
{{< highlight "java" >}}
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
```

