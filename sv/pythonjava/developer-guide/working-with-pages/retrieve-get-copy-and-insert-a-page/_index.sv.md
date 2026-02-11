---
title: Hämta, hämta, kopiera och infoga en sida
type: docs
weight: 10
url: /sv/python-java/retrieve-get-copy-and-insert-a-page/
---
## **Hämtar sidinformation**
I Microsoft Visio är sidorna antingen förgrunds- eller bakgrundssidor. För att få sidinformation, till exempel sid-ID och sidnamn, måste du först fastställa om en sida är en bakgrunds- eller förgrundssida.

Objektet `Page` representerar ritytan på en förgrundssida eller en bakgrundssida. Egenskapen Pages som exponeras av klassen `Diagram` stöder en samling av sidobjekt. Den här egenskapen kan användas för att hämta sidinformation.

Använd egenskapen `Page.Background` för att avgöra om en sida är en förgrunds- eller bakgrundssida.

### **Hämta sidinformation Programmeringsexempel**
Följande kodbit hämtar sidornas information från en diagram.


{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Call the diagram constructor to load diagram
diagram = Diagram("RetrievePageInfo.vdx")

for page in diagram.getPages():
    # Checks if current page is a background page
    if page.getBackground() == BOOL.TRUE:
        # Display information about the background page
        print("Background Page ID : " + str(page.getID()))
        print("Background Page Name : " + str(page.getName()))
    else:
        # Display information about the foreground page
        print("\nPage ID : " + str(page.getID()))
        print("Universal Name : " + str(page.getNameU()))
        print("ID of the Background Page : " + str(page.getBackPage()))

jpype.shutdownJVM()

{{< /highlight >}}


## **Hämta sidan Visio från en Diagram**
Ibland behöver utvecklare få en Visio-ritning med siddetaljer. Aspose.Diagram för Python via Java har funktioner som hjälper dem att göra detta.

Aspose.Diagram för Python via Java erbjuder klassen `Diagram` som representerar en Visio ritning. Egenskapen Pages som exponeras av klassen Diagram stöder en samling av `Page` objekt. Klassen PageCollection exponerar metoden `getPage` som kan anropas för att hämta Page-objekt.

### **Skaffa ett Visio sidobjekt med ID**
Detta exempel fungerar enligt följande:

1. Skapa ett objekt av klassen Diagram.
1. Ring Diagram.Pages-klassens getPage-metod.

Följande exempel visar hur man får ett sidobjekt med id från Visio-ritning.

#### **Hämta sidobjekt med ID-programmeringsexempel**

{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Call the diagram constructor to load diagram from a VDX file
diagram = Diagram("DrawingFlowCharts.vsdx")

# Set page id
page_id = 2
# Get page object by id
page2 = diagram.getPages().getPage(page_id)

jpype.shutdownJVM()

{{< /highlight >}}


### **Skaffa ett Visio sidobjekt efter namn**
Detta exempel fungerar enligt följande:

1. Skapa ett objekt av klassen Diagram.
1. Ring Diagram.Pages-klassens GetPage-metod.

#### **Hämta Sidobjekt efter namn Programmeringsexempel**
Följande exempel visar hur man får ett sidobjekt efter namn från Visio-ritning.


{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Call the diagram constructor to load diagram from a VSDX file
diagram = Diagram("DrawingFlowCharts.vsdx")

# Set page name
pageName = "Flow 2"
# Get page object by name
page2 = diagram.getPages().getPage(pageName)

jpype.shutdownJVM()

{{< /highlight >}}


## **Kopiera en Visio-sida till en annan Diagram**
Aspose.Diagram för Python via Java API tillåter utvecklare att kopiera och lägga till dess innehåll från den ena Visio diagram till en annan. Det här hjälpämnet förklarar hur du utför denna uppgift.

Aspose.Diagram för Python via Java API har klassen `Diagram` som representerar en Visio ritning. Egenskapen Pages som exponeras av klassen Diagram stöder en samling av `Page` objekt. Klassen PageCollection exponerar metoden `add` som kan anropas för att lägga till ytterligare ett Page-objekt.

Detta exempel fungerar enligt följande:

1. Skapa ett nytt objekt i klassen Diagram.
1. Ladda ett befintligt Visio diagram i klassobjektet Diagram.
1. Lägg till alla masters från den laddade Visio diagram
1. Hämta sidobjekt från den inlästa diagram (som måste kopieras).
1. Ställ in sidobjektets namn och id.
1. Ta bort den tomma sidan av den nya diagram (valfritt).
1. Anrop add-metoden för klassen PageCollection.
1. Spara den nya diagram i datorlagringen.

### **Kopiera ett Visio Sidprogrammeringsexempel**
Kodexemplet nedan visar hur man kopierar ett Visio sidobjekt till en annan Visio ritning.


{{< highlight python >}}
import jpype
import asposediagram

jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Call the diagram constructor to load diagram from a VSD file
originalDiagram = Diagram("Drawing1.vsdx")

# initialize the new visio diagram
newDiagram = Diagram()

# add all masters from the source Visio diagram
originalMasters = originalDiagram.getMasters()
for master in originalMasters:
    newDiagram.addMaster(originalDiagram, master.getName())

# get the page object from the original diagram
SrcPage = originalDiagram.getPages().getPage("Page-1")
# set page name
SrcPage.setName("new page")

# it calculates max page id
max_page_id = 0
if newDiagram.getPages().getCount() != 0:
    max_page_id = newDiagram.getPages().get(0).getID()

for i in range(0, newDiagram.getPages().getCount() - 1):
    if max_page_id < newDiagram.getPages().get(i).getID():
        max_page_id = newDiagram.getPages().get(i).getID()

MaxPageId = max_page_id
# set page id
SrcPage.setID(MaxPageId)
# add reference of the original diagram page
newDiagram.getPages().add(SrcPage)

# remove first empty page
newDiagram.getPages().remove(newDiagram.getPages().get(0))

# save diagram in VDX format
newDiagram.save("CopyVisioPage_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}


## **Kopiera Visio sida till en annan sidinstans**
Metoden `copy` i klassen `Page` tar en sidinstans att klona.

``` python
# import diagram

diagram = Diagram(dataDir + "Drawing1.vsdx")

newPage = Page()

# copy page

newPage.copy(diagram.getPages().getPage("Page-1"))

```

## **Infoga en tom sida i en Visio-ritning**
Aspose.Diagram för Python via Java kan infoga en ny tom sida i Microsoft Office Visio ritningen. Det här exemplet beskriver hur du gör det.

Metoden `add`, exponerad av Pages-samlingen, tillåter utvecklare att lägga till en ny tom sida i Visio diagram. Sid-ID bör tilldelas.

### **Infoga ett programmeringsexempel på tom sida**
Följande kodbit infogar en tom sida i Visio-ritningen:


{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load diagram
diagram = Diagram("Drawing1.vsdx")
        
# it calculates max page id
max_page_id = 0
if diagram.getPages().getCount() != 0:
    max_page_id = diagram.getPages().get(0).getID()

for i in range(0, diagram.getPages().getCount() - 1):
    if max_page_id < diagram.getPages().get(i).getID():
        max_page_id = diagram.getPages().get(i).getID()
        
# Initialize a new page object
newPage = Page()
# Set name
newPage.setName("new page")
# Set page ID
newPage.setID(max_page_id + 1)

# Or try the Page constructor
# Page newPage = Page(MaxPageId + 1)

# Add a new blank page
diagram.getPages().add(newPage)

# Save diagram
diagram.save("InsertBlankPageInVisio_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}


## **Flytta sidposition i Visio-ritningen**
Aspose.Diagram för Python via Java API kan flytta sidpositionen i Visio-ritningen. Metoden `moveTo`, exponerad av klassen `Page`, hjälper utvecklare att flytta sidpositionen.

### **Flytta Sidposition Programmeringsexempel**
MoveTo-medlemmen tar målsideindexet som en parameter för att flytta sidans position i Visio-ritningen:

``` python
# import diagram

diagram = Diagram(dataDir + "Drawing1.vsdx")

newPage = Page(1)

# move page in the diagram

newPage.moveTo(2)

diagram.save(dataDir + "Drawing1.vsdx", SaveFileFormat.VSDX)
```
