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
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Comments-AddPageLevelCommentInVisio-AddPageLevelCommentInVisio.java" >}}
## **Modificare un commento a livello di pagina nel Visio Diagram**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/)API supporta la modifica del commento a livello di pagina nella pagina di disegno Visio che viene presentata da un'icona nell'angolo in alto a sinistra della pagina.
### **Modifica commento**
La proprietà Comment, esposta dalla classe Annotation, consente agli sviluppatori di modificare i commenti nella pagina di disegno Visio.
#### **Modifica esempio di programmazione dei commenti**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Comments-EditPageLevelCommentInVisio-EditPageLevelCommentInVisio.java" >}}
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
