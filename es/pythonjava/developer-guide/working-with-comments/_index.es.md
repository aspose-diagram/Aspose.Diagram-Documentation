---
title: Trabajar con comentarios
type: docs
weight: 210
url: /es/python-java/working-with-comments/
description: Esta página describe cómo agregar un comentario en una página del dibujo Visio con la biblioteca Aspose.Diagram.
---
## **Agregue un comentario a nivel de página en el Visio**
Aspose.Diagram for Python via Java API allows developers to add comment anywhere on a page of [el dibujo Visio](DrawingComment.vsdx).
### **Agregar comentario**
El método addComment, expuesto por la clase Page, le permite agregar comentarios a una página de dibujo. Toma las coordenadas X e Y junto con una cadena de comentarios.

Microsoft Visio users add comments to the entire page that are presented by an icon in the upper-left corner of the page. Developers can add page level comments in the Visio. Aspose.Diagram for Python via Java API additionally supports to alter the page level comment in the Visio.
#### **Agregar ejemplo de programación de comentarios a nivel de página**
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
## **Edite un comentario de nivel de página en el Visio Diagram**
Aspose.Diagram for Python via Java API has support of altering the page-level comment on [el dibujo Visio](DrawingComment.vsdx) página que se presentan mediante un icono en la esquina superior izquierda de la página.
### **Editar comentario**
La propiedad Comentario, expuesta por la clase Anotación, permite a los desarrolladores editar comentarios en la página de dibujo Visio.
#### **Editar comentario Ejemplo de programación**
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
## **Agregue un comentario de nivel de forma en el dibujo Visio**
Aspose.Diagram for Python via Java API allows developers to add comments to the shape in [el dibujo Visio](DrawingComment.vsdx).
### **Agregar comentario**
Un método addComment sobrecargado, expuesto por la clase Page, toma una instancia de la clase Shape y una cadena de texto del comentario.
#### **Agregar ejemplo de programación de comentarios de nivel de forma**
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
