---
title: Placera automatiskt en samling former på sidan Visio
type: docs
weight: 30
url: /sv/python-java/auto-space-a-collection-of-shapes-in-the-visio-page/
---
## **Placera automatiskt en samling former på sidan Visio**
Med Aspose.Diagram för Python via Java API kan utvecklare automatiskt placera en samling former i Visio-ritningen. För att uppnå detta erbjuder klassen `Page` `autoSpaceShapes`-medlem som tar parametrarna ShapeCollection och AutoSpaceOptions. Klassen `AutoSpaceOptions` gör det möjligt att ställa in horisontella och vertikala avstånd.

### **Auto-space former på sidan**
Använd följande kod i din ansökan för att automatiskt fördela en samling former på valfri sida i Visio-ritningen.

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
