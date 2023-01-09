---
title: Lavorare con i commenti
type: docs
weight: 220
url: /it/net/working-with-comments/
description: Questa pagina descrive come aggiungere o modificare commenti con la libreria Aspose.Diagram.
---
## **Aggiungi un commento a livello di pagina in Visio**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/)API consente agli sviluppatori di inserire commenti ovunque nella pagina di disegno Visio.
### **Aggiungi un commento**
 Il metodo AddComment, esposto da[Pagina](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class, consente agli sviluppatori di aggiungere commenti a una pagina di disegno. Prende le coordinate X e Y insieme a una stringa di commento.
#### **Aggiungi commento Esempio di programmazione**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Comments-AddPageLevelCommentInVisio-AddPageLevelCommentInVisio.cs" >}}
## **Modificare un commento a livello di pagina nel Visio Diagram**
 Microsoft Visio gli utenti aggiungono commenti all'intera pagina che sono presentati da un'icona nell'angolo in alto a sinistra della pagina. Gli sviluppatori possono[aggiungere commenti a livello di pagina nel Visio](/pages/createpage.action?spaceKey=diagramnet&title=Add+a+Page-Level+Comment+in+the+Visio&linkCreation=true&fromPageId=18350768). [Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API supporta inoltre la modifica del commento a livello di pagina nel Visio.
### **Modifica commento**
 La proprietà Comment, esposta da[Annotazione](http://www.aspose.com/api/net/diagram/aspose.diagram/annotation) class, consente agli sviluppatori di modificare i commenti nella pagina di disegno Visio.
#### **Modifica esempio di programmazione dei commenti**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Comments-EditPageLevelCommentInVisio-EditPageLevelCommentInVisio.cs" >}}
## **Aggiungere un commento a livello di forma nel disegno Visio**
[Aspose.Diagram for .NET](https://www.aspose.com/products/diagram/net)API consente agli sviluppatori di aggiungere commenti alla forma in un disegno Visio.
### **Aggiungi un commento**
Un metodo AddComment in overload, esposto da[Pagina](http://www.aspose.com/api/net/diagram/aspose.diagram/page)class accetta un'istanza della classe Shape e una stringa di testo del commento.
#### **Aggiungi commento Esempio di programmazione**
**C#**

{{< highlight "java" >}}

 // load diagram

Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

// retrieve page by name

Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// retrieve shape by ID

Aspose.Diagram.Shape shape = page.Shapes.GetShape(12);

page.AddComment(shape, "Hello");

// save diagram

diagram.Save(@"c:\temp\Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
