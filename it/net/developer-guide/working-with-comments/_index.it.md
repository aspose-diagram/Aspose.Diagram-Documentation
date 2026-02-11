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

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioComments();

// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Add comment
diagram.Pages[0].AddComment(7.205905511811023, 3.880708661417323, "test@");

// Save diagram
diagram.Save(dataDir + "AddComment_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Modificare un commento a livello di pagina nel Visio Diagram**
 Microsoft Visio gli utenti aggiungono commenti all'intera pagina che sono presentati da un'icona nell'angolo in alto a sinistra della pagina. Gli sviluppatori possono[aggiungere commenti a livello di pagina nel Visio](/pages/createpage.action?spaceKey=diagramnet&title=Add+a+Page-Level+Comment+in+the+Visio&linkCreation=true&fromPageId=18350768). [Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API supporta inoltre la modifica del commento a livello di pagina nel Visio.
### **Modifica commento**
 La proprietà Comment, esposta da[Annotazione](http://www.aspose.com/api/net/diagram/aspose.diagram/annotation) class, consente agli sviluppatori di modificare i commenti nella pagina di disegno Visio.
#### **Modifica esempio di programmazione dei commenti**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioComments();

// Load Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get collection of the annotations
AnnotationCollection annotations = diagram.Pages.GetPage("Page-1").PageSheet.Annotations;

// Iterate through the annotations
foreach (Annotation annotation in annotations)
{
    string comment = annotation.Comment.Value;
    comment += "Updation mark";
    annotation.Comment.Value = comment;
}
// Save Visio
diagram.Save(dataDir + "EditComment_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

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
