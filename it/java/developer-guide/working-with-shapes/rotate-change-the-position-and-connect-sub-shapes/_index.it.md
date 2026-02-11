---
title: Ruota, cambia la posizione e collega le forme secondarie
type: docs
weight: 60
url: /it/java/rotate-change-the-position-and-connect-sub-shapes/
---
## **Ruota una forma con l'angolo adatto**
 Aspose.Diagram for Java consente di ruotare una forma a qualsiasi angolazione. Il metodo SetAngle esposto da[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class può essere utilizzato per ruotare una forma a qualsiasi angolo desiderato. Prende un singolo parametro come angolo.
### **Ruotare un esempio di programmazione delle forme**
Utilizzare il seguente codice nell'applicazione Java per ruotare una forma utilizzando Aspose.Diagram for Java.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RotateVisioShape.class); 
// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-3");
// get shape by id
Shape shape = page.getShapes().getShape(16);

// Add a shape and set the angle
shape.setAngle(190);

// Save diagram
diagram.save(dataDir + "RotateVisioShape_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Modificare la posizione di una forma**
La classe Shape consente di modificare la posizione di una forma. La linea del connettore si regola automaticamente quando la forma viene spostata in una posizione diversa.

I metodi Move e MoveTo, esposti dalla classe Shape, supportano o meno la modifica della posizione di una forma come parte di un gruppo.
Gli esempi di codice in questo articolo spostano una forma nella pagina.
**Inserisci diagram** 

![cose da fare:immagine_alt_testo](http://i.imgur.com/cThgWnB.png)


**Il diagram dopo che la forma è stata spostata** 

![cose da fare:immagine_alt_testo](http://i.imgur.com/Q3QByqe.png)

Il processo per spostare una forma è:

1. Carica un diagram.
1. Trova una forma particolare.
1. Sposta la forma in una posizione diversa
1. Salva lo diagram.
### **Esempio di programmazione della modifica della posizione**
Il frammento di codice seguente mostra come spostare la forma. Il codice recupera una pagina Visio per nome e forma per ID 16 e ne sposta la posizione.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(MoveVisioShape.class);  
// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-3");
// get shape by id
Shape shape = page.getShapes().getShape(16);
// move shape from its position, it adds values in coordinates
shape.move(1, 1);

// save diagram
diagram.save(dataDir + "MoveVisioShape_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Collega le forme secondarie dei gruppi**
Questo argomento elabora come collegare due forme secondarie di due diverse forme di gruppo nei diagrammi Microsoft Visio utilizzando Aspose.Diagram for Java.

 Il metodo ConnectShapesViaConnector esposto da[Pagina](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) class può essere utilizzata per connettere le forme tramite i loro ID. Il metodo AddShape, esposto da[Diagram](https://reference.aspose.com/diagram/java)class, può essere utilizzato per aggiungere una forma.

|<p>**L'ingresso diagram** </p><p>![cose da fare:immagine_alt_testo](http://i.imgur.com/74rDby5.png)</p>|<p>**Il diagram dopo il collegamento di sotto-forme** </p><p>![cose da fare:immagine_alt_testo](http://i.imgur.com/c387dZJ.png)</p>|
|:- |:- |
Il codice seguente mostra come:

1. Carica un file di esempio.
1. Accedi a una determinata pagina.
1. Aggiungi la forma del connettore dinamico alla pagina selezionata.
1. Connetti sotto-forme
### **Esempio di programmazione Connect Sub-shapes**
Utilizzare il seguente codice nell'applicazione Java per collegare le forme secondarie di due diverse forme di gruppo utilizzando Aspose.Diagram for Java.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ConnectVisioSubShapes.class);   
// set sub shape ids
long shapeFromId = 2;
long shapeToId = 4;

// load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// access a particular page
Page page = diagram.getPages().getPage("Page-3");
       
// initialize connector shape
Shape shape = new Shape();
shape.getLine().getEndArrow().setValue(4);
shape.getLine().getLineWeight().setValue(0.01388);

// add shape
long connecter1Id = diagram.addShape(shape, "Dynamic connector", page.getID());
// connect sub-shapes
page.connectShapesViaConnector(shapeFromId, ConnectionPointPlace.RIGHT, shapeToId, ConnectionPointPlace.LEFT, connecter1Id);
// save Visio drawing
diagram.save(dataDir + "ConnectVisioSubShapes_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Ottieni le forme collegate a una forma particolare**
[Aggiungi e collega Visio Forme](/diagram/it/java/add-and-connect-visio-shapes/) spiega come aggiungere una forma e collegarla ad altre forme nei diagrammi Microsoft Visio utilizzando Aspose.Diagram for Java. È anche possibile trovare forme collegate a una forma specifica.

 Il metodo ConnectedShapes esposto da[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class può essere utilizzata per ottenere gli ID delle forme connesse a una forma. Il metodo GetShape, esposto da[Collezione Shape](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shapecollection) class, può quindi essere utilizzato per trovare una forma in base al relativo ID.

Il codice seguente mostra come:

1. Carica un file di esempio.
1. Accedi a una forma particolare.
1. Ottieni i nomi di tutte le forme collegate alla forma selezionata.
### **Ottieni un esempio di programmazione di forme**
Usa il seguente codice nella tua applicazione Java per trovare tutte le forme collegate a una forma specifica usando Aspose.Diagram for Java.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetAllConnectedShapes.class);
// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get shape by id
Shape shape = diagram.getPages().getPage("Page-3").getShapes().getShape(16);
// get connected shapes
long[] connectedShapeIds = shape.connectedShapes(ConnectedShapesFlags.CONNECTED_SHAPES_ALL_NODES, null);

for (long id : connectedShapeIds)
{
    shape = diagram.getPages().getPage("Page-3").getShapes().getShape(id);
    System.out.println("ID: " + shape.getID() + "\t\t Name: " + shape.getName());
}

{{< /highlight >}}
```
