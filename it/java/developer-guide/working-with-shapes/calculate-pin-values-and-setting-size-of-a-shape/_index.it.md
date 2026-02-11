---
title: Calcola i valori dei pin e imposta le dimensioni di una forma
type: docs
weight: 40
url: /it/java/calculate-pin-values-and-setting-size-of-a-shape/
---
## **Calcola i valori PinX e PinY della forma secondaria**
 Se la forma è un figlio della forma di gruppo, la sua xform è una coordinata relativa della sua forma genitore, ma non una coordinata assoluta nel[Pagina](https://reference.aspose.com/diagram/java/com.aspose.diagram/page). Se l'utente richiede di ottenere la coordinata assoluta, allora questo codice di esempio aiuta.

Un punto specificato nelle coordinate locali può essere convertito in coordinate padre applicando le seguenti trasformazioni nel seguente ordine:

1. Sottrai il valore della proprietà LocPinX dell'elemento Cell_Type dalla coordinata x.
1. Sottrai il valore della proprietà LocPinY di Cell_Type dalla coordinata y.
1. Eseguire il mirroring del punto sull'asse y se il valore della proprietà FlipX di Cell_Type è uguale a uno.
1. Eseguire il mirroring del punto sull'asse x se il valore della proprietà FlipY di Cell_Type è uguale a uno.
1. Ruotare il punto in senso antiorario attorno all'origine in base al valore della proprietà Angle di Cell_Type.
1. Aggiungi il valore di PinX Cell_Type alla coordinata x.
1. Aggiungi il valore di PinY Cell_Type alla coordinata y.
### **Calcola il campione di programmazione PinX e PinY**
Utilizzare il seguente codice nell'applicazione Java per calcolare i valori PinX e PinY di una forma secondaria utilizzando Aspose.Diagram for Java API.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CalculateCenterOfSubShapes.class);
        
// load Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get group shape
Shape shape = diagram.getPages().get(0).getShapes().getShape(138);
// get sub-shape of the group shape
Shape subShape = shape.getShapes().getShape(140);


AffineTransform m = new AffineTransform();
// apply the translation vector
m.translate(-(float)subShape.getXForm().getLocPinX().getValue(), -(float)subShape.getXForm().getLocPinY().getValue());		
// set the elements of that matrix to a rotation
m.rotate((float)subShape.getXForm().getAngle().getValue());
// apply the translation vector
m.translate((float)subShape.getXForm().getPinX().getValue(), (float)subShape.getXForm().getPinY().getValue());

// get pinx and piny		
double pinx = m.getTranslateX();
double piny = m.getTranslateY();
		
// calculate the sub-shape pinx and piny
double resultx = shape.getXForm().getPinX().getValue() - shape.getXForm().getLocPinX().getValue() - pinx;
double resulty = shape.getXForm().getPinY().getValue() - shape.getXForm().getLocPinY().getValue() - piny;

{{< /highlight >}}

## **Impostazione dell'altezza e della larghezza di una forma**
 Il[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) La classe consente di controllare le dimensioni della forma specificando l'altezza e la larghezza della forma utilizzando i metodi SetHeight e SetWidth.

 I metodi SetHeight e SetWidth, esposti da[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape)class, supporta il ridimensionamento di una forma con il master, senza il master o sotto forma di una forma di gruppo.

Gli esempi di codice in questo articolo impostano l'altezza e la larghezza per ridimensionare la forma nella pagina.

**Inserisci diagram** 

![cose da fare:immagine_alt_testo](http://i.imgur.com/cTiNWa7.png)

**Il diagram dopo l'altezza e la larghezza sono stati modificati**

![cose da fare:immagine_alt_testo](calculate-pin-values-and-setting-size-of-a-shape_1.png)

Il processo per impostare l'altezza e la larghezza è:

1. Carica un diagram.
1. Trova una forma particolare.
1. Imposta l'altezza di una forma.
1. Imposta la larghezza di una forma.
1. Salva lo diagram.
### **Impostazione dell'altezza e della larghezza Esempio di programmazione**
Il frammento di codice seguente mostra come impostare l'altezza e la larghezza della forma. Il codice cerca un rettangolo con il nome della forma, con l'ID forma 1, e ne imposta l'altezza e la larghezza su double.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ChangeShapeSize.class);
        
// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");
// get shape by id
Shape shape = page.getShapes().getShape(796);
// alter the size of Shape
shape.setWidth(2 * shape.getXForm().getWidth().getValue());
shape.setHeight(2 * shape.getXForm().getHeight().getValue());
// save diagram
diagram.save(dataDir + "ChangeShapeSize_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

