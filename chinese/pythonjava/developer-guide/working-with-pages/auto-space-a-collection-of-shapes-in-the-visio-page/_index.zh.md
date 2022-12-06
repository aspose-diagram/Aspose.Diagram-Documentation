---
title: 在 Visio 页面中自动放置一组形状
type: docs
weight: 30
url: /zh/python-java/auto-space-a-collection-of-shapes-in-the-visio-page/
---
## **在 Visio 页面中自动放置一组形状**
通过 Java API 为 Python 使用 Aspose.Diagram，开发人员可以在 Visio 绘图中自动放置一组形状。为了实现这一点，`Page` 类提供了 `autoSpaceShapes` 成员，该成员采用 ShapeCollection 和 AutoSpaceOptions 参数。 `AutoSpaceOptions` 类允许设置水平和垂直距离。

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
