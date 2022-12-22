---
title: Spaziatura automatica una raccolta di forme nella pagina Visio
type: docs
weight: 30
url: /it/python-java/auto-space-a-collection-of-shapes-in-the-visio-page/
---
## **Spaziatura automatica una raccolta di forme nella pagina Visio**
With Aspose.Diagram for Python via Java API, developers can auto-space a collection of shapes in the Visio drawing. In order to achieve this, the `Page` class offers `autoSpaceShapes` member which takes ShapeCollection and AutoSpaceOptions parameters. The `AutoSpaceOptions` class allows to set horizontal and vertical distances.

### **Spaziatura automatica forme nella pagina**
Utilizzare il codice seguente nell'applicazione per eseguire la spaziatura automatica di una raccolta di forme in qualsiasi pagina del disegno Visio.

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
