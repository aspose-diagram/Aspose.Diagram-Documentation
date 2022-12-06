---
title: Spaziatura automatica una raccolta di forme nella pagina Visio
type: docs
weight: 30
url: /it/python-java/auto-space-a-collection-of-shapes-in-the-visio-page/
---
## **Spaziatura automatica una raccolta di forme nella pagina Visio**
Con Aspose.Diagram per Python tramite Java API, gli sviluppatori possono spaziare automaticamente una raccolta di forme nel disegno Visio. Per raggiungere questo obiettivo, la classe `Page` offre il membro `autoSpaceShapes` che accetta i parametri ShapeCollection e AutoSpaceOptions. La classe `AutoSpaceOptions` permette di impostare distanze orizzontali e verticali.

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
