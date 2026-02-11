---
title: Lavorare con i collegamenti ipertestuali
type: docs
weight: 110
url: /it/java/working-with-hyperlinks/
---
## **Aggiungi collegamento ipertestuale a una forma Visio**
È un approccio semplice aggiungere un collegamento ipertestuale alla forma Microsoft Visio in modo dinamico.

Nei disegni multipagina Visio, i collegamenti ipertestuali possono spostarti da una pagina all'altra. Puoi anche collegare il tuo disegno a una pagina web oa un file sul tuo sistema.

Queste proprietà sono esposte dal[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) la classe supporta il[com.aspose.diagram.Hyperlink](https://reference.aspose.com/diagram/java/com.aspose.diagram/hyperlink) oggetto. Il metodo add può essere usato per aggiungere i dati del collegamento ipertestuale di una forma.

Per identificare le proprietà in Microsoft Visio:

1. In un diagram, fare clic con il pulsante destro del mouse su una forma.
1.  Selezionare**Collegamento ipertestuale**.
1. Imposta le proprietà esistenti
1.  Premere**OK** pulsante

**I dati del collegamento ipertestuale di una forma, come mostrato in Microsoft Visio**

![cose da fare:immagine_alt_testo](working-with-hyperlinks_1.png)

I frammenti di codice seguenti aggiungono i dati del collegamento ipertestuale della forma.
### **Aggiungi esempio di programmazione di collegamenti ipertestuali**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AddHyperlinkToShape.class);   
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");
// get shape by ID
Shape shape = page.getShapes().getShape(2);

//initialize Hyperlink object
Hyperlink hyperlink = new Hyperlink();
//set address value
hyperlink.getAddress().setValue("http://www.google.com/");
//set sub address value
hyperlink.getSubAddress().setValue("Sub address here");
//set description value
hyperlink.getDescription().setValue("Description here");
//set name
hyperlink.setName("MyHyperLink");

//add hyperlink to the shape
shape.getHyperlinks().add(hyperlink);            
//save diagram to local space
diagram.save(dataDir + "AddHyperlinkToShape_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Ottieni i dati dei collegamenti ipertestuali delle forme Visio**
 È possibile ottenere i dati del collegamento ipertestuale di una forma in modo simile a te[leggendo i dati di forma Visio]().

Gli sviluppatori possono recuperare tutti i collegamenti ipertestuali da una forma Visio allo stesso modo di loro[leggi i dati della forma Visio]() utilizzando[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/)

Nei disegni multipagina Visio, i collegamenti ipertestuali possono spostarti da una pagina all'altra. Puoi anche collegare il tuo disegno a una pagina web oa un file sul tuo sistema.

Queste proprietà sono esposte dal[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) la classe supporta il[com.aspose.diagram.Hyperlink](https://reference.aspose.com/diagram/java/com.aspose.diagram/hyperlink)oggetto. La proprietà può essere usata per leggere i dati del collegamento ipertestuale di una forma.

Per identificare le proprietà in Microsoft Visio:

1. In un diagram, fare clic con il pulsante destro del mouse su una forma.
1.  Selezionare**Collegamento ipertestuale.**
 Tutte le proprietà esistenti sono elencate nella finestra di dialogo.

**I dati del collegamento ipertestuale di una forma, come mostrato in Microsoft Visio**

![cose da fare:immagine_alt_testo](working-with-hyperlinks_2.png)

**Una finestra della console che mostra l'output dei dati della forma**

![cose da fare:immagine_alt_testo](working-with-hyperlinks_3.png)

I frammenti di codice seguenti leggono i dati del collegamento ipertestuale della forma.
### **Ottieni un esempio di programmazione dei collegamenti ipertestuali**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetHyperlinks.class);  
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");
// get shape by ID
Shape shape = page.getShapes().getShape(1);
// iterate through the hyperlinks
for (Hyperlink hyperlink :(Iterable<Hyperlink>) shape.getHyperlinks())
{
    System.out.println("Address: " + hyperlink.getAddress().getValue());
    System.out.println("Sub Address: " + hyperlink.getSubAddress().getValue());
    System.out.println("Description: " + hyperlink.getDescription().getValue());
}

{{< /highlight >}}

