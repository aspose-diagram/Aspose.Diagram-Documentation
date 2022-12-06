---
title: Автоматическое размещение коллекции фигур на странице Visio
type: docs
weight: 30
url: /ru/python-java/auto-space-a-collection-of-shapes-in-the-visio-page/
---
## **Автоматическое размещение коллекции фигур на странице Visio**
С Aspose.Diagram для Python через Java API разработчики могут автоматически размещать набор фигур в чертеже Visio. Для этого класс `Page` предлагает член `autoSpaceShapes`, который принимает параметры ShapeCollection и AutoSpaceOptions. Класс `AutoSpaceOptions` позволяет задавать горизонтальные и вертикальные расстояния.

### **Авто-пространство фигур на странице**
Используйте следующий код в своем приложении для автоматического размещения набора фигур на любой странице чертежа Visio.

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
