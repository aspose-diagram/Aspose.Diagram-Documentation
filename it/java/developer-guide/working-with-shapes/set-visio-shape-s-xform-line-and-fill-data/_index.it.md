---
title: Imposta i dati XForm, Line e Fill di Visio Shape
type: docs
weight: 70
url: /it/java/set-visio-shape-s-xform-line-and-fill-data/
---
## **Impostazione dei dati XForm**
 L'elemento XForm fa parte dello schema XML Microsoft Visio. XForm specifica la posizione di una forma, ad esempio larghezza, altezza, rotazione e se la forma è stata capovolta. Il[XForm](https://reference.aspose.com/diagram/java/com.aspose.diagram/xform) proprietà, esposto dal[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class, supporta l'oggetto Aspose.Diagram.XForm. La proprietà XForm può essere utilizzata per recuperare o aggiornare i dati XForm di una forma. Gli esempi di codice in questo articolo modificano i valori XForm PinX (coordinata X) e PinY (coordinata Y) per spostare le forme sulla pagina.

**Inserisci diagram** 

![cose da fare:immagine_alt_testo](set-visio-shape-s-xform-line-and-fill-data_1.png)

**Lo diagram dopo il** **PinX** **e** **Pin Y** **i valori sono stati modificati** 

![cose da fare:immagine_alt_testo](set-visio-shape-s-xform-line-and-fill-data_2.png)

Il processo per l'aggiornamento dei dati XForm è:

1. Carica un diagram.# Trova una forma particolare.# Aggiorna i dati XForm della forma.
1. Salva lo diagram.
### **Esempio di programmazione**
Il frammento di codice seguente mostra come aggiornare i dati XForm di una forma. Il codice cerca un processo per i nomi delle forme, con l'ID forma 1, e ne imposta le coordinate X e Y su 5.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetXFormdata.class); 
// call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "SetXFormdata.vsd");

//Find a particular shape and update its XForm
for(Shape shape :(Iterable<Shape>) diagram.getPages().get(0).getShapes())
{
    if (shape.getNameU().toLowerCase() == "process" && shape.getID() == 1)
    {
        shape.getXForm().getPinX().setValue(5);
        shape.getXForm().getPinY().setValue(5);
    }
}
// save diagram
diagram.save(dataDir + "SetXFormdata_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Impostare Visio dati linea di forma**
Le forme possono essere formattate in diversi modi. Questo articolo mostra come specificare gli attributi di una linea.

Microsoft Visio consente agli utenti di formattare le righe in vari modi. Aspose.Diagram for Java supporta:

- Peso: lo spessore di una linea.
- Colore: imposta il colore della linea della forma.
- Line Color Transparency: imposta la trasparenza del colore della linea della forma in percentuale.
- Motivo: definisce se la linea è continua, tratteggiata o ha un altro motivo.
- Arrotondamento: il raggio degli angoli.
- Frecce di inizio e fine: specificato se la linea ha frecce.
- Dimensioni freccia iniziale e finale: imposta le dimensioni della freccia.
- Cap: termina l'arrotondamento della linea.
### **Modifica il colore della linea, lo spessore, il tipo di trattino, la trasparenza, l'arrotondamento, il tipo di freccia e la dimensione della freccia del bordo di una forma**
 Il[Linea](https://reference.aspose.com/diagram/java/com.aspose.diagram/line) proprietà, esposto dal[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)class, supporta l'oggetto Aspose.Diagram.Line. Questa proprietà può essere utilizzata per recuperare o aggiornare i dati della linea di una forma.
#### **Esempio di programmazione dei dati di linea**
La parte di codice seguente aggiorna i dati della linea di shape.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetLineData.class);

// load a Visio diagram
Diagram diagram = new Diagram(dataDir + "SetLineData.vsd");
// get the page by its name
Page page1 = diagram.getPages().getPage("Page-1");
// get shape by its ID
Shape shape = page1.getShapes().getShape(1);
// set line dash type by index
shape.getLine().getLinePattern().setValue(4);
// set line weight, defualt in PT
shape.getLine().getLineWeight().setValue(2);
// set color of the shape's line
shape.getLine().getLineColor().getUfe().setF("RGB(95,108,53)");
// set line rounding, default in inch
shape.getLine().getRounding().setValue(0.3125);
// set line caps
shape.getLine().getLineCap().setValue(BOOL.TRUE);
// set line color transparency in percent
shape.getLine().getLineColorTrans().setValue(50);

/* add arrows to the connector or curve shapes */
// select arrow type by index
shape.getLine().getBeginArrow().setValue(4);
shape.getLine().getEndArrow().setValue(4);
// set arrow size 
shape.getLine().getBeginArrowSize().setValue(ArrowSizeValue.LARGE);
shape.getLine().getBeginArrowSize().setValue(ArrowSizeValue.LARGE);

// save the Visio
diagram.save(dataDir + "SetLineData_Out.vsdx", SaveFileFormat.VSDX);
// save diagram
diagram.save(dataDir+ "output.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
## **Impostare Visio dati di riempimento della forma**
Le forme possono essere formattate in diversi modi. Questo argomento descrive come specificare il riempimento di una forma.

 Microsoft Office Visio consente agli utenti di formattare i riempimenti in vari modi. Il[Riempire](https://reference.aspose.com/diagram/java/com.aspose.diagram/fill) classe del Aspose.Diagram for Java API supporta l'impostazione:

- Colori di sfondo e di primo piano.
- Trasparenza.
- Modelli di riempimento.
- Ombre.
### **Impostazione dei valori di riempimento**
La proprietà Fill, esposta dalla classe Shape, supporta l'oggetto Aspose.Diagram.Fill. La proprietà Fill può essere utilizzata per recuperare o aggiornare i dati di riempimento di una forma.

|<p>**L'ingresso diagram** </p><p>![cose da fare:immagine_alt_testo](http://i.imgur.com/OrhEecb.png)</p>|<p>**Il diagram dopo aver cambiato il colore di riempimento** </p><p>![cose da fare:immagine_alt_testo](http://i.imgur.com/HO0wmZ8.png)</p>|
|:- |:- |
#### **Esempio di programmazione dei dati di riempimento**
Il frammento di codice seguente aggiorna i dati di riempimento di una forma. Il codice cerca una forma denominata rettangolo, con ID forma 1, e imposta i colori di sfondo e primo piano del riempimento.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetFillData.class);


//Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir+ "Drawing1.vsd");

//Find a particular shape and update its XForm
for (com.aspose.diagram.Shape shape : (Iterable<Shape>) diagram.getPages().get(0).getShapes())
{
    if (shape.getNameU().toLowerCase() == "rectangle" && shape.getID() == 1)
    {
        shape.getFill().getFillBkgnd().setValue(diagram.getPages().getPage(0).getShapes().getShape(0).getFill().getFillBkgnd().getValue());
        shape.getFill().getFillForegnd().setValue("#ebf8df");
    }
}
// save diagram
diagram.save(dataDir+ "SetFillData_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
### **Recupera i dati di riempimento ereditati di una forma Visio**
Le forme Visio possono ereditare lo stile padre e la forma principale. Gli sviluppatori possono ottenere o impostare i dati di riempimento ereditati di una forma Visio. La proprietà InheritFill, esposta dalla classe Shape, contiene i valori di formattazione del riempimento per la forma ereditata dallo stile padre e dalla forma principale.
#### **Esempio di programmazione dei dati di riempimento ereditati Recupera**
Il seguente frammento di codice recupera i dati di riempimento ereditati della forma. Si prega di controllare questo codice di esempio:

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveInheritedFillData.class) + "Shapes/";

// Call the diagram constructor to load a VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get page by ID
Page page = diagram.getPages().getPage("Page-1");
// Get shape by ID
Shape shape = page.getShapes().getShape(1);
// Get the fill formatting values
System.out.println(shape.getInheritFill().getFillBkgnd().getValue());
System.out.println(shape.getInheritFill().getFillForegnd().getValue());
System.out.println(shape.getInheritFill().getFillPattern().getValue());
System.out.println(shape.getInheritFill().getShapeShdwObliqueAngle().getValue());
System.out.println(shape.getInheritFill().getShapeShdwOffsetX().getValue());
System.out.println(shape.getInheritFill().getShapeShdwOffsetY().getValue());
System.out.println(shape.getInheritFill().getShapeShdwScaleFactor().getValue());
System.out.println(shape.getInheritFill().getShapeShdwType().getValue());
System.out.println(shape.getInheritFill().getShdwBkgnd().getValue());
System.out.println(shape.getInheritFill().getShdwBkgndTrans().getValue());
System.out.println(shape.getInheritFill().getShdwForegnd().getValue());
System.out.println(shape.getInheritFill().getShdwForegndTrans().getValue());
System.out.println(shape.getInheritFill().getShdwPattern().getValue());

{{< /highlight >}}
```
