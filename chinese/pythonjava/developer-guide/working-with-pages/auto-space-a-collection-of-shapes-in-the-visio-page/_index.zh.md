---
title: 在 Visio 页面中自动放置一组形状
type: docs
weight: 30
url: /zh/python-java/auto-space-a-collection-of-shapes-in-the-visio-page/
---
## **在 Visio 页面中自动放置一组形状**
With Aspose.Diagram for Python via Java API, developers can auto-space a collection of shapes in the Visio drawing. In order to achieve this, the `Page` class offers `autoSpaceShapes` member which takes ShapeCollection and AutoSpaceOptions parameters. The `AutoSpaceOptions` class allows to set horizontal and vertical distances.

### **页面中的自动空间形状**
在您的应用程序中使用以下代码在 Visio 绘图的任何页面中自动放置一组形状。

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
