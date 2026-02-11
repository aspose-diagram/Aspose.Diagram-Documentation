---
title: Recupera, ottieni, copia e inserisci una pagina
type: docs
weight: 10
url: /it/python-java/retrieve-get-copy-and-insert-a-page/
---
## **Recupero delle informazioni sulla pagina**
In Microsoft Visio, le pagine sono in primo piano o in secondo piano. Per ottenere informazioni sulla pagina, ad esempio l'ID della pagina e il nome della pagina, stabilire innanzitutto se una pagina è una pagina di sfondo o in primo piano.

L'oggetto `Page` rappresenta l'area di disegno di una pagina in primo piano o di una pagina di sfondo. La proprietà Pages esposta dalla classe `Diagram` supporta una raccolta di oggetti Page. Questa proprietà può essere utilizzata per recuperare informazioni sulla pagina.

Utilizzare la proprietà `Page.Background` per determinare se una pagina è in primo piano o in background.

### **Recupera il campione di programmazione delle informazioni sulla pagina**
Il seguente pezzo di codice recupera le informazioni sulle pagine da un diagram.


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


## **Ottieni la pagina Visio da uno Diagram**
Sometimes, developers need to get a Visio drawing's page details. Aspose.Diagram for Python via Java has features that helps them do this.

Aspose.Diagram for Python via Java offers the `Diagram` class that represents a Visio drawing. The Pages property exposed by the Diagram class supports a collection of `Page` objects. The PageCollection class exposes `getPage` method that can be called to get Page object.

### **Ottenere un oggetto pagina Visio per ID**
Questo esempio funziona come segue:

1. Creare un oggetto della classe Diagram.
1. Chiamare il metodo getPage della classe Diagram.Pages.

L'esempio seguente mostra come ottenere un oggetto pagina in base all'ID dal disegno Visio.

#### **Esempio di programmazione Ottieni oggetto pagina per ID**

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


### **Ottenere un oggetto pagina Visio per nome**
Questo esempio funziona come segue:

1. Creare un oggetto della classe Diagram.
1. Chiamare il metodo GetPage della classe Diagram.Pages.

#### **Esempio di programmazione Ottieni oggetto pagina per nome**
L'esempio seguente mostra come ottenere un oggetto pagina per nome dal disegno Visio.


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


## **Copia una pagina Visio in un'altra Diagram**
Aspose.Diagram for Python via Java API allows developers to copy and add its content from the one Visio diagram to another. This help topic explains how to accomplish this task.

Aspose.Diagram for Python via Java API has the `Diagram` class that represents a Visio drawing. The Pages property exposed by the Diagram class supports a collection of `Page` objects. The PageCollection class exposes `add` method that can be called to add another Page object.

Questo esempio funziona come segue:

1. Crea un nuovo oggetto della classe Diagram.
1. Carica un Visio diagram esistente nell'oggetto classe Diagram.
1. Aggiungi tutti i master dal Visio diagram caricato
1. Ottieni l'oggetto della pagina dallo diagram caricato (che deve essere copiato).
1. Imposta il nome e l'id dell'oggetto della pagina.
1. Rimuovere la pagina vuota del nuovo diagram (facoltativo).
1. Chiama il metodo add della classe PageCollection.
1. Salvare il nuovo diagram nella memoria del computer.

### **Copia un esempio di programmazione della pagina Visio**
L'esempio di codice seguente mostra come copiare un oggetto pagina Visio in un altro disegno Visio.


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


## **Copia Visio Page in un'altra istanza di Page**
Il metodo `copy` della classe `Page` accetta un'istanza di pagina da clonare.

``` python
# import diagram

diagram = Diagram(dataDir + "Drawing1.vsdx")

newPage = Page()

# copy page

newPage.copy(diagram.getPages().getPage("Page-1"))

```

## **Inserisci una pagina vuota in un disegno Visio**
Aspose.Diagram for Python via Java can insert a new blank page into the Microsoft Office Visio drawing. This example topic describes how to do so.

Il metodo `add`, esposto dalla raccolta Pages, consente agli sviluppatori di aggiungere una nuova pagina vuota in Visio diagram. L'ID pagina deve essere assegnato.

### **Inserisci un esempio di programmazione in una pagina vuota**
La seguente parte di codice inserisce una pagina vuota nel disegno Visio:


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


## **Sposta la posizione della pagina nel disegno Visio**
Aspose.Diagram for Python via Java API can move page position in the Visio drawing. The `moveTo` method, exposed by the `Page` class, helps developers to move the page position.

### **Sposta Posizione pagina Esempio di programmazione**
Il membro MoveTo utilizza l'indice della pagina di destinazione come parametro per spostare la posizione della pagina nel disegno Visio:

``` python
# import diagram

diagram = Diagram(dataDir + "Drawing1.vsdx")

newPage = Page(1)

# move page in the diagram

newPage.moveTo(2)

diagram.save(dataDir + "Drawing1.vsdx", SaveFileFormat.VSDX)
```
