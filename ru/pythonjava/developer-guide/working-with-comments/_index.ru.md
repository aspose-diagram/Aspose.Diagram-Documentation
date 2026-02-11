---
title: Работа с комментариями
type: docs
weight: 210
url: /ru/python-java/working-with-comments/
description: На этой странице описывается, как добавить комментарий на страницу чертежа Visio с помощью библиотеки Aspose.Diagram.
---
## **Добавьте комментарий на уровне страницы в Visio**
 Aspose.Diagram для Python via Java API позволяет разработчикам добавлять комментарии в любом месте на странице[чертеж Visio](DrawingComment.vsdx).
### **Добавить комментарий**
Метод addComment, предоставляемый классом Page, позволяет добавлять комментарии на страницу рисования. Он принимает координаты X и Y вместе со строкой комментария.

Microsoft Visio пользователи добавляют комментарии ко всей странице, которые представлены значком в верхнем левом углу страницы. Разработчики могут добавлять комментарии на уровне страницы в Visio. Aspose.Diagram для Python via Java API дополнительно поддерживает изменение комментария на уровне страницы в Visio.
#### **Пример программирования добавления комментариев на уровне страницы**
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
## **Редактировать комментарий на уровне страницы в Visio Diagram**
Aspose.Diagram для Python via Java API поддерживает изменение комментария на уровне страницы[чертеж Visio](DrawingComment.vsdx) страницы, которые представлены значком в верхнем левом углу страницы.
### **Редактировать комментарий**
Свойство Comment, предоставляемое классом Annotation, позволяет разработчикам редактировать комментарии на странице рисования Visio.
#### **Пример программирования редактирования комментариев**
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
## **Добавление комментария на уровне формы в чертеже Visio**
 Aspose.Diagram для Python via Java API позволяет разработчикам добавлять комментарии к форме в[чертеж Visio](DrawingComment.vsdx).
### **Добавить комментарий**
Перегруженный метод addComment, предоставляемый классом Page, принимает экземпляр класса Shape и текстовую строку комментария.
#### **Пример программирования добавления комментариев на уровне формы**
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
