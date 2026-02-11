---
title: Raggruppa, converti e verifica le forme
type: docs
weight: 50
url: /it/java/group-convert-and-verify-shapes/
---
## **Raggruppa più forme insieme nel disegno Visio**
Aspose.Diagram API consente agli sviluppatori di raggruppare le forme insieme per spostarle tutte in una volta. Ogni forma in un gruppo mantiene un'identità univoca e ha il proprio insieme di proprietà. Quando cambiamo la formattazione di un gruppo di forme, assegna la nuova proprietà a ciascuna forma.
### **Come raggruppare le forme**
Il metodo Group esposto dalla classe ShapeCollection può essere utilizzato per raggruppare le forme.

Il codice seguente mostra come:

1. Carica un campione diagram.
1. inizializzato un array delle forme
1. ottenere una forma particolare per id.
1. ottieni un'altra particolare forma particolare per id.
1. assegnare forme all'array.
1. raggruppare le forme chiamando il metodo Group.
1. salvo diagram
#### **Esempio di programmazione delle forme di gruppo**
Utilizzare il seguente codice nell'applicazione Java per raggruppare le forme utilizzando Aspose.Diagram for Java API.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GroupShapes.class);
// load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-3");

// Initialize an array of shapes
Shape[] ss = new Shape[3];

// extract and assign shapes to the array
ss[0] = page.getShapes().getShape(15);
ss[1] = page.getShapes().getShape(16);
ss[2] = page.getShapes().getShape(17);

// mark array shapes as group
page.getShapes().group(ss);

// save visio diagram
diagram.save(dataDir + "GroupShapes_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Converti una forma Visio in altri formati di file**
Aspose.Diagram for Java API consente agli sviluppatori di convertire una singola forma Visio in qualsiasi altro formato di file supportato. In questo articolo rimuoviamo tutte le altre forme Visio dalla pagina e personalizziamo le impostazioni della pagina in base alla dimensione della forma di origine.
### **Conversione di una particolare forma Visio**
Developers can convert a Visio shape to PDF, HTML, Image, SVG, and SWF by [specificando le opzioni di salvataggio Visio]().
Questo codice di esempio funziona come segue:

1. Carica una fonte Visio.
1. Ottieni una pagina particolare.
1. Rimuovi la pagina di sfondo.
1. Costruisci una tabella hash di tutte le forme che contengono gli ID e i nomi.
1. Itera attraverso la tabella hash
1. Rimuovi tutte le forme dalla pagina Visio, tranne quella in particolare.
1. Imposta la dimensione della pagina.
1. Salva la pagina Visio in qualsiasi formato di file supportato.
#### **Esempio di programmazione di forme convertite**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SaveVisioShapeInOtherFormats.class);   
        
double shapeWidth = 0;
double shapeHeight = 0;

// call a Diagram class constructor to load the VSDX diagram
Diagram srcVisio = new Diagram(dataDir + "Drawing1.vsdx");
// get Visio page
Page srcPage = srcVisio.getPages().get(1);
// remove background page
srcPage.setBackPage(null);

// get hash table of shapes, it holds id and name
Hashtable<Long, String> remShapes = new Hashtable<Long, String>();
for (Shape shape : (Iterable<Shape>)srcPage.getShapes())
    // for the normal shape
    remShapes.put(shape.getID(), shape.getName());
        

// iterate through the hash table
Enumeration<Long> enumKey = remShapes.keys();
while(enumKey.hasMoreElements())
{
    Long key = enumKey.nextElement();
    String val = remShapes.get(key);
    Shape shape = srcPage.getShapes().getShape(key);
    // check of the shape name
    if(val.equals("GroupShape1"))
    {
        // move shape to the origin corner
        shapeWidth = shape.getXForm().getWidth().getValue();
        shapeHeight = shape.getXForm().getHeight().getValue();
        shape.moveTo(shapeWidth*0.5, shapeHeight*0.5);
        // trim page size
        srcPage.getPageSheet().getPageProps().getPageWidth().setValue(shapeWidth);
        srcPage.getPageSheet().getPageProps().getPageHeight().setValue(shapeHeight);
    }
    else
    {
        // remove shape from the Visio page and hash table
        srcPage.getShapes().remove(shape);
        remShapes.remove(key);
    }
}

// specify saving options
PdfSaveOptions opts = new PdfSaveOptions();
// set page count to save
opts.setPageCount(1);
// set starting index of the page
opts.setPageIndex(1);
// save it
srcVisio.save(dataDir + "SaveVisioShapeInOtherFormats_Out.pdf", opts);

{{< /highlight >}}

### **Convert Visio Shape to PDF**
The ToPdf method of the Shape class allows to convert a shape into the PDF format.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toPdf(dataDir + "out.pdf");

{{< /highlight >}}
### **Convert Visio Shape to HTML**
The ToHTML method of the Shape class allows to convert a shape into the HTML format.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

HTMLSaveOptions hs = new HTMLSaveOptions();

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toHTML(dataDir + "out.pdf", hs);

{{< /highlight >}}

{{% alert color="primary" %}} 

 Accogliamo con favore le vostre domande e suggerimenti a[Aspose.Diagram Foro](https://forum.aspose.com/c/diagram/17). Ti risponderemo prontamente.

{{% /alert %}} 
## **Verifica se due forme Visio sono collegate o incollate**
 Aspose.Diagram for Java API consente agli sviluppatori di verificare che le due forme Visio siano incollate o collegate. In precedenza, abbiamo visto come collegare o incollare due forme in questi argomenti della guida:[Aggiungi e collega Visio Forme](/diagram/it/java/add-and-connect-visio-shapes/) e[Forme di colla all'interno del contenitore](/diagram/it/java/working-with-shapes-gluing/).
### **Verifica delle Forme Connesse o Incollate**
 Il[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) offre le proprietà IsGlued e IsConnected per determinare se due forme sono collegate o connesse.
#### **Esempio di programmazione per la verifica di forme connesse o incollate**
La parte di codice seguente verifica se due forme sono connesse o incollate.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(VerifyConnectedOrGluedShapes.class);  
// call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// set two shape ids
long ShapeIdOne = 15;
long ShapeIdTwo = 16;

// get Visio page by name
Page page = diagram.getPages().getPage("Page-3");

// get Visio shapes by ids
Shape ShapedOne = page.getShapes().getShape(ShapeIdOne);
Shape ShapedTwo = page.getShapes().getShape(ShapeIdTwo);

// determine whether shapes are connected
boolean connected = ShapedOne.isConnected(ShapedTwo);
System.out.println("Shapes are connected: " + connected);

// determine whether shapes are glued
boolean glued = ShapedOne.isGlued(ShapedTwo);
System.out.println("Shapes are Glued: " + glued);

{{< /highlight >}}

## **Verificare se la forma Visio si trova in un gruppo di forme**
Aspose.Diagram for Java API consente agli sviluppatori di verificare se la forma Visio si trova o meno in un gruppo di forme.
### **Verifica della forma nel gruppo delle forme**
La classe Shape offre proprietà IsInGroup per determinare se la forma Visio è in una forma di gruppo.
#### **Verifica della forma nell'esempio di programmazione del gruppo di forme**
La parte di codice seguente verifica se la forma è in una forma di gruppo.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveTheParentShape.class) + "Shapes\\";
				
// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a sub-shape by page name, group shape ID, and then sub-shape ID
Shape shape = diagram.getPages().getPage("Page-3").getShapes().getShape(13).getShapes().getShape(2);
System.out.println("Is it in a Group: " + shape.isInGroup());
{{< /highlight >}}


{{% alert color="primary" %}} 

 Accogliamo con favore le vostre domande e suggerimenti a[Aspose.Diagram Foro](https://forum.aspose.com/c/diagram/17). Ti risponderemo prontamente.

{{% /alert %}}
