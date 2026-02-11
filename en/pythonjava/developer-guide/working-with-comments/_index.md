---
title: Working with Comments
type: docs
weight: 210
url: /python-java/working-with-comments/
description: This page describes how to add comment on a page of the Visio drawing with Aspose.Diagram library.
---

## **Add a Page-Level Comment in the Visio**
Aspose.Diagram for Python via Java API allows developers to add comment anywhere on a page of [the Visio drawing](DrawingComment.vsdx).
### **Add Comment**
The addComment method, exposed by the Page class, allows you to add comments to a drawing page. It takes the X and Y coordinates along with a comment string.

Microsoft Visio users add comments to the entire page that are presented by an icon in the upper-left corner of the page. Developers can add page level comments in the Visio. Aspose.Diagram for Python via Java API additionally supports to alter the page level comment in the Visio.
#### **Add Page-Level Comment Programming Sample**
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
## **Edit a Page-Level Comment in the Visio Diagram**
Aspose.Diagram for Python via Java API has support of altering the page-level comment on [the Visio drawing](DrawingComment.vsdx) page which are presented by an icon in the upper-left corner of the page. 
### **Edit Comment**
The Comment property, exposed by the Annotation class, allows developers to edit comments in the Visio drawing page.
#### **Edit Comment Programming Sample**
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
## **Add a Shape-Level Comment in Visio Drawing**
Aspose.Diagram for Python via Java API allows developers to add comments to the shape in [the Visio drawing](DrawingComment.vsdx).
### **Add Comment**
An overloaded addComment method, exposed by the Page class takes a Shape class instance and text string of the comment.
#### **Add Shape-Level Comment Programming Sample**
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
