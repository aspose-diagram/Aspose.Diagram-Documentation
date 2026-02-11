---
title: Arbeiten mit Kommentaren
type: docs
weight: 210
url: /de/python-java/working-with-comments/
description: Auf dieser Seite wird beschrieben, wie Sie einer Seite der Zeichnung Visio mit der Bibliothek Aspose.Diagram einen Kommentar hinzufügen.
---
## **Fügen Sie einen Kommentar auf Seitenebene in Visio hinzu**
Aspose.Diagram for Python via Java API allows developers to add comment anywhere on a page of [die Zeichnung Visio](DrawingComment.vsdx).
### **Einen Kommentar hinzufügen**
Die addComment-Methode, die von der Page-Klasse bereitgestellt wird, ermöglicht das Hinzufügen von Kommentaren zu einem Zeichenblatt. Es nimmt die X- und Y-Koordinaten zusammen mit einer Kommentarzeichenfolge.

Microsoft Visio users add comments to the entire page that are presented by an icon in the upper-left corner of the page. Developers can add page level comments in the Visio. Aspose.Diagram for Python via Java API additionally supports to alter the page level comment in the Visio.
#### **Programmierbeispiel für Kommentare auf Seitenebene hinzufügen**
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
## **Bearbeiten Sie einen Kommentar auf Seitenebene im Visio Diagram**
Aspose.Diagram for Python via Java API has support of altering the page-level comment on [die Zeichnung Visio](DrawingComment.vsdx) Seite, die durch ein Symbol in der oberen linken Ecke der Seite dargestellt werden.
### **Kommentar bearbeiten**
Die Comment-Eigenschaft, die von der Annotation-Klasse verfügbar gemacht wird, ermöglicht Entwicklern das Bearbeiten von Kommentaren auf dem Zeichenblatt Visio.
#### **Programmierbeispiel für Kommentar bearbeiten**
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
## **Fügen Sie in der Zeichnung Visio einen Kommentar auf Formebene hinzu**
Aspose.Diagram for Python via Java API allows developers to add comments to the shape in [die Zeichnung Visio](DrawingComment.vsdx).
### **Einen Kommentar hinzufügen**
Eine überladene addComment-Methode, die von der Page-Klasse verfügbar gemacht wird, übernimmt eine Shape-Klasseninstanz und eine Textzeichenfolge des Kommentars.
#### **Beispiel für die Programmierung von Kommentaren auf Formebene hinzugefügt**
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
