---
title: Arbeta med kommentarer
type: docs
weight: 210
url: /sv/python-java/working-with-comments/
description: Den här sidan beskriver hur man lägger till kommentarer på en sida i Visio-ritningen med Aspose.Diagram-biblioteket.
---
## **Lägg till en kommentar på sidnivå i Visio**
 Aspose.Diagram för Python via Java API tillåter utvecklare att lägga till kommentarer var som helst på en sida med[Visio ritningen](DrawingComment.vsdx).
### **Lägg till kommentar**
Metoden addComment, exponerad av klassen Page, låter dig lägga till kommentarer på en ritsida. Den tar X- och Y-koordinaterna tillsammans med en kommentarsträng.

Microsoft Visio användare lägger till kommentarer på hela sidan som presenteras av en ikon i det övre vänstra hörnet på sidan. Utvecklare kan lägga till kommentarer på sidnivå i Visio. Aspose.Diagram för Python via Java API stödjer dessutom att ändra sidnivåkommentaren i Visio.
#### **Lägg till programmeringsexempel på sidnivåkommentarer**
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
## **Redigera en kommentar på sidnivå i Visio Diagram**
Aspose.Diagram för Python via Java API har stöd för att ändra sidnivåkommentaren på[Visio ritningen](DrawingComment.vsdx) sida som presenteras av en ikon i det övre vänstra hörnet på sidan.
### **Redigera kommentar**
Egenskapen Comment, exponerad av klassen Annotation, tillåter utvecklare att redigera kommentarer på ritsidan Visio.
#### **Redigera kommentar Programmeringsexempel**
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
## **Lägg till en kommentar på formnivå i Visio Ritning**
 Aspose.Diagram för Python via Java API tillåter utvecklare att lägga till kommentarer till formen i[Visio ritningen](DrawingComment.vsdx).
### **Lägg till kommentar**
En överbelastad addComment-metod, som exponeras av klassen Page, tar en Shape-klassinstans och textsträng av kommentaren.
#### **Lägg till programmeringsexempel för kommentar på formnivå**
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
