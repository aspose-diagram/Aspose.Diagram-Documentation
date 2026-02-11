---
title: Lavorare con l'incollaggio di forme
type: docs
weight: 10
url: /it/java/working-with-shapes-gluing/
---
## **Ottieni i connettori incollati a una forma particolare**
[Aggiungi e collega Visio Forme](/diagram/it/java/add-and-connect-visio-shapes/) spiega come aggiungere una forma e collegarla ad altre forme nei diagrammi Microsoft Visio utilizzando Aspose.Diagram for Java. È anche possibile trovare connettori incollati a questa forma.
### **Ottenere forme incollate**
 Il metodo GluedShapes esposto da[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)class può essere utilizzata per ottenere un elenco degli ID di tutti i connettori associati a una forma oppure, se la forma in questione è un connettore, gli ID delle forme a cui è connessa. Il metodo GetShape, esposto dalla[Collezione Shape](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shapecollection) class, può quindi essere utilizzato per trovare una forma in base al relativo ID.

Il codice seguente mostra come:

1. Carica un file di esempio.
1. Accedi a una forma particolare.
1. Ottieni un elenco di ID di tutti i connettori incollati a questa forma.
#### **Ottieni un esempio di programmazione di connettori incollati**
Usa il seguente codice nella tua applicazione Java per trovare tutti i connettori incollati a una forma usando Aspose.Diagram for Java.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetGluedConnectors.class);   
// call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "RetrieveShapeInfo.vsd");
// get shape by an ID
Shape shape = diagram.getPages().get(0).getShapes().getShape(90);
// get all glued 1D shapes
long[] gluedShapeIds = shape.gluedShapes(GluedShapesFlags.GLUED_SHAPES_ALL_1_D, null, null);

// display shape ID and name
for (long id : gluedShapeIds)
{
    shape = diagram.getPages().get(0).getShapes().getShape(id);
    System.out.println("ID: " + shape.getID() + "\t\t Name: " + shape.getName());
}

{{< /highlight >}}

## **Colla Visio Forme insieme al punto di connessione**
Aspose.Diagram for Java consente agli sviluppatori di incollare forme insieme attraverso i punti di connessione.
### **Forme di colla**
 Il metodo GlueShapes esposto da[Pagina](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) classe può essere utilizzata.

|<p>**Inserisci diagram** </p><p>![cose da fare:immagine_alt_testo](http://i.imgur.com/Z69f4hg.png)</p>|<p>**Lo diagram dopo aver incollato le sagome** </p><p>![cose da fare:immagine_alt_testo](http://i.imgur.com/5TJpDwc.png)</p>|
|:- |:- |
Il codice seguente mostra come:

1. Carica un file di esempio.
1. Forme di colla.
1. Salva diagram.
#### **Colla Visio Esempio di programmazione delle forme**
Usa il seguente codice nella tua applicazione Java per incollare le forme attraverso i punti di connessione:


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GlueVisioShapes.class);
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get a particular page
Page page = diagram.getPages().getPage("Page-1");
// set shape id
long shape1_ID = 7;
long shape2_ID = 494;
// Glue shapes
page.glueShapes(shape1_ID, ConnectionPointPlace.CENTER, shape2_ID);

// Save diagram
diagram.save(dataDir + "GlueVisioShapes_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Forme di colla all'interno del contenitore**
Aspose.Diagram for Java consente agli sviluppatori di incollare forme di gruppo all'interno di un contenitore.
### **Forma del gruppo di colla**
È possibile utilizzare il metodo GlueShapesInContainer esposto dalla classe Page.

|<p>**Inserisci diagram** </p><p>![cose da fare:immagine_alt_testo](http://i.imgur.com/HRRzIEh.png)</p>|<p>**Lo diagram dopo aver incollato le sagome di gruppo** </p><p>![cose da fare:immagine_alt_testo](http://i.imgur.com/YxCiOgU.png)</p>|
|:- |:- |
Il codice seguente mostra come:

1. Carica un file di esempio.
1. Incolla le forme del gruppo.
1. Salva diagram.
#### **Forme di colla all'interno dell'esempio di programmazione**
Usa il seguente codice nella tua applicazione Java per incollare la forma del gruppo all'interno di un contenitore:


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GlueContainerShape.class);   
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get a particular page
Page page = diagram.getPages().getPage("Page-1");

// The ID of shape which is glue from Aspose.Diagram.Shape.
long shapeFromId = 779;
// The location on the first connection index where to glue
int shapeToBeginConnectionIndex = 72;
// The location on the end connection index where to glue
int shapeToEndConnectionIndex = 73;
// The ID of shape where to glue to Aspose.Diagram.Shape.
long shapeToId = 743;

// Glue shapes in container
page.glueShapesInContainer(shapeFromId, shapeToBeginConnectionIndex, shapeToEndConnectionIndex, shapeToId);

// Glue shapes in container using connection name
// page.GlueShapesInContainer(fasId, "U05L", "U05R", cabinetId1);

// Save diagram
diagram.save(dataDir + "GlueContainerShape_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

