---
title: Lavorare con i commenti
type: docs
weight: 210
url: /it/python-java/working-with-comments/
description: Questa pagina descrive come aggiungere un commento ad una pagina del disegno Visio con libreria Aspose.Diagram.
---
## **Aggiungi un commento a livello di pagina in Visio**
Aspose.Diagram for Python via Java API allows developers to add comment anywhere on a page of [il disegno Visio](DrawingComment.vsdx).
### **Aggiungi un commento**
Il metodo addComment, esposto dalla classe Page, consente di aggiungere commenti a una pagina di disegno. Prende le coordinate X e Y insieme a una stringa di commento.

Microsoft Visio users add comments to the entire page that are presented by an icon in the upper-left corner of the page. Developers can add page level comments in the Visio. Aspose.Diagram for Python via Java API additionally supports to alter the page level comment in the Visio.
#### **Aggiungi un esempio di programmazione dei commenti a livello di pagina**
```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Call the diagram constructor to load diagram
diagram = Diagram("DrawingComment.vsdx")

# Add comment
diagram.getPages().getPage(0).addComment(7.205905511811023, 3.880708661417323, "test@")

# Save diagram
diagram.save("AddPageLevelCommentInVisio_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}
```
## **Modificare un commento a livello di pagina nel Visio Diagram**
Aspose.Diagram for Python via Java API has support of altering the page-level comment on [il disegno Visio](DrawingComment.vsdx) pagina che sono presentati da un'icona nell'angolo in alto a sinistra della pagina.
### **Modifica commento**
La proprietà Comment, esposta dalla classe Annotation, consente agli sviluppatori di modificare i commenti nella pagina di disegno Visio.
#### **Modifica esempio di programmazione dei commenti**
```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load Visio
diagram = Diagram("DrawingComment.vsdx")

# get collection of the annotations
annotations = diagram.getPages().getPage("Page-1").getPageSheet().getAnnotations()

# iterate through the annotations
for annotation in annotations:
    comment = annotation.getComment().getValue()
    comment += "Updation mark"
    annotation.getComment().setValue(comment)

# save Visio
diagram.save("EditPageLevelCommentInVisio_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}
```
## **Aggiungere un commento a livello di forma nel disegno Visio**
Aspose.Diagram for Python via Java API allows developers to add comments to the shape in [il disegno Visio](DrawingComment.vsdx).
### **Aggiungi un commento**
Un metodo addComment sottoposto a overload, esposto dalla classe Page accetta un'istanza della classe Shape e una stringa di testo del commento.
#### **Aggiungere un esempio di programmazione di commenti a livello di forma**
```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load diagram
diagram = Diagram("DrawingComment.vsdx")

# retrieve page by name
page = diagram.getPages().getPage("Page-1")

# retrieve shape by ID
shape = page.getShapes().getShape(1)

page.addComment(shape, "Hello")

# save diagram
diagram.save("AddShapeLevelCommentInVisio_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}
```
