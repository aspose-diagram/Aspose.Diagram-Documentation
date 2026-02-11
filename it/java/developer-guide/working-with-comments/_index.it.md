---
title: Lavorare con i commenti
type: docs
weight: 210
url: /it/java/working-with-comments/
---
## **Aggiungi un commento a livello di pagina in Visio**
Aspose.Diagram for Java API consente agli sviluppatori di aggiungere commenti ovunque su una pagina del disegno Visio.
### **Aggiungi un commento**
Il metodo addComment, esposto dalla classe Page, consente di aggiungere commenti a una pagina di disegno. Prende le coordinate X e Y insieme a una stringa di commento.

 Microsoft Visio gli utenti aggiungono commenti all'intera pagina che sono presentati da un'icona nell'angolo in alto a sinistra della pagina. Gli sviluppatori possono[aggiungere commenti a livello di pagina nel Visio](). [Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API supporta inoltre la modifica del commento a livello di pagina nel Visio.
#### **Aggiungi commento Esempio di programmazione**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AddPageLevelCommentInVisio.class);
// Call the diagram constructor to load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Add comment
diagram.getPages().getPage(0).addComment(7.205905511811023, 3.880708661417323, "test@");

// Save diagram
diagram.save(dataDir + "AddPageLevelCommentInVisio_Out.vdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Modificare un commento a livello di pagina nel Visio Diagram**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/)API supporta la modifica del commento a livello di pagina nella pagina di disegno Visio che viene presentata da un'icona nell'angolo in alto a sinistra della pagina.
### **Modifica commento**
La proprietà Comment, esposta dalla classe Annotation, consente agli sviluppatori di modificare i commenti nella pagina di disegno Visio.
#### **Modifica esempio di programmazione dei commenti**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(EditPageLevelCommentInVisio.class);
// load Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get collection of the annotations
AnnotationCollection annotations = diagram.getPages().getPage("Page-1").getPageSheet().getAnnotations();

// iterate through the annotations
for (Annotation annotation : (Iterable<Annotation>) annotations) 
{
    String comment = annotation.getComment().getValue();
    comment += "Updation mark";
    annotation.getComment().setValue(comment);
}
// save Visio
diagram.save(dataDir + "EditPageLevelCommentInVisio_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Aggiungere un commento a livello di forma nel disegno Visio**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/)API consente agli sviluppatori di aggiungere commenti alla forma in un disegno Visio.
### **Aggiungi un commento**
Un metodo addComment sottoposto a overload, esposto dalla classe Page accetta un'istanza della classe Shape e una stringa di testo del commento.
#### **Aggiungi commento Esempio di programmazione**
**Java**

{{< highlight "java" >}}

 // load diagram

Diagram diagram = new Diagram("c:\\temp\\Drawing1.vsdx");

// retrieve page by name

Page page = diagram.getPages().getPage("Page-1");

// retrieve shape by ID

Shape shape = page.getShapes().getShape(12);

page.addComment(shape, "Hello");

// save diagram

diagram.save("c:\\temp\\Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
