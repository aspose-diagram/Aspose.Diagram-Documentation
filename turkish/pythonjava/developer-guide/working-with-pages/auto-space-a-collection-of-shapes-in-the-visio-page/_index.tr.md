---
title: Visio Sayfasında Şekil Koleksiyonunu Otomatik Olarak Arala
type: docs
weight: 30
url: /tr/python-java/auto-space-a-collection-of-shapes-in-the-visio-page/
---
## **Visio Sayfasında Şekil Koleksiyonunu Otomatik Olarak Arala**
With Aspose.Diagram for Python via Java API, developers can auto-space a collection of shapes in the Visio drawing. In order to achieve this, the `Page` class offers `autoSpaceShapes` member which takes ShapeCollection and AutoSpaceOptions parameters. The `AutoSpaceOptions` class allows to set horizontal and vertical distances.

### **Sayfadaki Şekilleri Otomatik Arala**
Use the following code in your application to auto-space a collection of shapes in any page of the Visio drawing.

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
