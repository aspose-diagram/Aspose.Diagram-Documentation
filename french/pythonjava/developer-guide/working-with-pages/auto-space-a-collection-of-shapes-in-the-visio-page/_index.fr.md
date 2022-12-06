---
title: Espacement automatique d'une collection de formes dans la page Visio
type: docs
weight: 30
url: /fr/python-java/auto-space-a-collection-of-shapes-in-the-visio-page/
---
## **Espacement automatique d'une collection de formes dans la page Visio**
With Aspose.Diagram for Python via Java API, developers can auto-space a collection of shapes in the Visio drawing. In order to achieve this, the `Page` class offers `autoSpaceShapes` member which takes ShapeCollection and AutoSpaceOptions parameters. The `AutoSpaceOptions` class allows to set horizontal and vertical distances.

### **Espacer automatiquement les formes dans la page**
Utilisez le code suivant dans votre application pour espacer automatiquement une collection de formes dans n'importe quelle page du dessin Visio.

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
