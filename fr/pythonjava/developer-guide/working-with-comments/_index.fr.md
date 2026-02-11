---
title: Travailler avec des commentaires
type: docs
weight: 210
url: /fr/python-java/working-with-comments/
description: Cette page décrit comment ajouter un commentaire sur une page du dessin Visio avec la bibliothèque Aspose.Diagram.
---
## **Ajouter un commentaire au niveau de la page dans le Visio**
Aspose.Diagram for Python via Java API allows developers to add comment anywhere on a page of [le dessin Visio](DrawingComment.vsdx).
### **Ajouter un commentaire**
La méthode addComment, exposée par la classe Page, permet d'ajouter des commentaires à une page de dessin. Il prend les coordonnées X et Y avec une chaîne de commentaire.

Microsoft Visio users add comments to the entire page that are presented by an icon in the upper-left corner of the page. Developers can add page level comments in the Visio. Aspose.Diagram for Python via Java API additionally supports to alter the page level comment in the Visio.
#### **Ajouter un exemple de programmation de commentaires au niveau de la page**

{{< highlight python >}}
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

## **Modifier un commentaire au niveau de la page dans le Visio Diagram**
Aspose.Diagram for Python via Java API has support of altering the page-level comment on [le dessin Visio](DrawingComment.vsdx) page qui sont présentés par une icône dans le coin supérieur gauche de la page.
### **Modifier le commentaire**
La propriété Comment, exposée par la classe Annotation, permet aux développeurs de modifier les commentaires dans la page de dessin Visio.
#### **Éditer un exemple de programmation de commentaire**

{{< highlight python >}}
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

## **Ajouter un commentaire au niveau de la forme dans le dessin Visio**
Aspose.Diagram for Python via Java API allows developers to add comments to the shape in [le dessin Visio](DrawingComment.vsdx).
### **Ajouter un commentaire**
Une méthode addComment surchargée, exposée par la classe Page prend une instance de classe Shape et la chaîne de texte du commentaire.
#### **Ajouter un exemple de programmation de commentaire au niveau de la forme**

{{< highlight python >}}
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

