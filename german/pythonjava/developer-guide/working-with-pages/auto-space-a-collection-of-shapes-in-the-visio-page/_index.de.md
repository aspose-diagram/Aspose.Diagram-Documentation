---
title: Platzieren Sie automatisch eine Sammlung von Formen auf der Seite Visio
type: docs
weight: 30
url: /de/python-java/auto-space-a-collection-of-shapes-in-the-visio-page/
---
## **Platzieren Sie automatisch eine Sammlung von Formen auf der Seite Visio**
Mit Aspose.Diagram für Python über Java API können Entwickler eine Sammlung von Formen in der Visio-Zeichnung automatisch platzieren. Um dies zu erreichen, bietet die Klasse `Page` den Member `autoSpaceShapes`, der ShapeCollection- und AutoSpaceOptions-Parameter übernimmt. Die Klasse `AutoSpaceOptions` ermöglicht die Einstellung horizontaler und vertikaler Abstände.

### **Formen mit automatischem Abstand auf der Seite**
Verwenden Sie den folgenden Code in Ihrer Anwendung, um eine Sammlung von Formen auf einer beliebigen Seite der Zeichnung Visio automatisch zu platzieren.

``` python
# load a Visio drawing

diagram = Diagram("Drawing1.vsdx")

# get page of the Visio drawing

page = diagram.getPages().getPage("Page-1")

# initialize auto space options

options = AutoSpaceOptions()

# set horizontal and vertical distances

options.setDistanceInHorizontal(2)

options.setDistanceInVertical(2)

# set auto space 

page.autoSpaceShapes(page.getShapes(), options)

# save Visio drawing

diagram.save("AutoSpaceShapes_Out.vsdx", SaveFileFormat.VSDX)

```
