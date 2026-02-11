---
title: Lavorare con l'incollaggio di forme
type: docs
weight: 40
url: /it/net/working-with-shapes-gluing/
description: Questa sezione spiega come ottenere forme incollate a una particolare forma con Aspose.Diagram.
---
## **Ottieni i connettori incollati a una forma particolare**
[Aggiungi e collega Visio Forme](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/) spiega come aggiungere una forma e collegarla ad altre forme nei diagrammi Microsoft Visio utilizzando Aspose.Diagram for .NET. È anche possibile trovare connettori incollati a questa forma.
### **Ottenere forme incollate**
 Il metodo GluedShapes esposto da[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)class può essere utilizzata per ottenere un elenco degli ID di tutti i connettori associati a una forma oppure, se la forma in questione è un connettore, gli ID delle forme a cui è connessa. Il metodo GetShape, esposto dalla[Collezione Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shapecollection) class, può quindi essere utilizzato per trovare una forma in base al relativo ID.

Il codice seguente mostra come:

1. Carica un file di esempio.
1. Accedi a una forma particolare.
1. Ottieni un elenco di ID di tutti i connettori incollati a questa forma.
#### **Ottieni un esempio di programmazione di connettori incollati**
Usa il seguente codice nella tua applicazione .NET per trovare tutti i connettori incollati a una forma usando Aspose.Diagram for .NET.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "RetrieveShapeInfo.vsd");
// Get shape by an ID
Shape shape = diagram.Pages[0].Shapes.GetShape(90);
// Get all glued 1D shapes
long[] gluedShapeIds = shape.GluedShapes(GluedShapesFlags.GluedShapesAll1D, null, null);

// Display shape ID and name
foreach (long id in gluedShapeIds)
{
    shape = diagram.Pages[0].Shapes.GetShape(id);
    Console.WriteLine("ID: " + shape.ID + "\t\t Name: " + shape.Name);
}

{{< /highlight >}}

## **Colla Visio Forme insieme al punto di connessione**
Aspose.Diagram for .NET consente agli sviluppatori di incollare forme insieme attraverso i punti di connessione.
### **Forme di colla**
 Il metodo GlueShapes esposto da[Pagina](http://www.aspose.com/api/net/diagram/aspose.diagram/page) classe può essere utilizzata.

|<p>**Inserisci diagram** </p><p>![cose da fare:immagine_alt_testo](working-with-shapes-gluing_1.png)</p>|<p>**Lo diagram dopo aver incollato le sagome** </p><p>![cose da fare:immagine_alt_testo](working-with-shapes-gluing_2.png)</p>|
|:- |:- |
Il codice seguente mostra come:

1. Carica un file di esempio.
1. Forme di colla.
1. Salva diagram.
#### **Colla Visio Esempio di programmazione delle forme**
Usa il seguente codice nella tua applicazione .NET per incollare le forme attraverso i punti di connessione:


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get a particular page
Page page = diagram.Pages.GetPage("Page-1");
// Set shape id
long shape1_ID = 7;
long shape2_ID = 494;
// Glue shapes
page.GlueShapes(shape1_ID, Aspose.Diagram.Manipulation.ConnectionPointPlace.Center, shape2_ID);

// Save diagram
diagram.Save(dataDir + "GlueVisioShapes_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Forme di colla all'interno del contenitore**
Aspose.Diagram for .NET consente agli sviluppatori di incollare forme di gruppo all'interno di un contenitore.
### **Forma del gruppo di colla**
 Il metodo GlueShapesInContainer esposto da[Pagina](http://www.aspose.com/api/net/diagram/aspose.diagram/page) classe può essere utilizzata.

|<p>**Inserisci diagram** </p><p>![cose da fare:immagine_alt_testo](working-with-shapes-gluing_3.png)</p>|<p>**Lo diagram dopo aver incollato le sagome di gruppo** </p><p>![cose da fare:immagine_alt_testo](working-with-shapes-gluing_4.png)</p>|
|:- |:- |
Il codice seguente mostra come:

1. Carica un file di esempio.
1. Incolla le forme del gruppo.
1. Salva diagram.
#### **Forme di colla all'interno dell'esempio di programmazione**
Usa il seguente codice nella tua applicazione .NET per incollare la forma del gruppo all'interno di un contenitore:


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get a particular page
Page page = diagram.Pages.GetPage("Page-1");

// The ID of shape which is glue from Aspose.Diagram.Shape.
long shapeFromId = 779;
// The location on the first connection index where to glue
int shapeToBeginConnectionIndex = 72;
// The location on the end connection index where to glue
int shapeToEndConnectionIndex = 73;
// The ID of shape where to glue to Aspose.Diagram.Shape.
long shapeToId = 743;

// Glue shapes in container
page.GlueShapesInContainer(shapeFromId, shapeToBeginConnectionIndex, shapeToEndConnectionIndex, shapeToId);

// Glue shapes in container using connection name
// Page.GlueShapesInContainer(fasId, "U05L", "U05R", cabinetId1);

// Save diagram
diagram.Save(dataDir + "GlueContainerShape_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

