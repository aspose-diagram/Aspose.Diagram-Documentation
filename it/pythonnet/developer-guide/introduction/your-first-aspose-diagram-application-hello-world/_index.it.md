---
title: Your First Aspose.Diagram Application - Hello World
type: docs
weight: 30
url: /it/python-net/your-first-aspose-diagram-application-hello-world/
---
{{% alert color="primary" %}}

This beginner's topic shows how developers can create a simple first application (Hello World) using Aspose.Diagram' simple API. The application creates a Microsoft Visio file with the words Hello World in the page.

{{% /alert %}}

### **Creating the Hello World Application**

To create the Hello World application using Aspose.Diagram API:

1. Creare un'istanza della classe Workbook.
1. Applica la licenza:
 1. Se hai acquistato una licenza, usa la licenza nella tua applicazione per ottenere l'accesso alla piena funzionalità di Aspose.Diagram
 1. Se stai utilizzando la versione di valutazione del componente (se stai utilizzando Aspose.Diagram senza licenza), salta questo passaggio.
1. Crea un nuovo file Microsoft Visio o apri un file esistente in cui desideri aggiungere/aggiornare del testo.
1.  Inserisci le parole**Hello World!** nella pagina a cui si accede.
1. Generare il file Microsoft Visio modificato.

Gli esempi seguenti illustrano i passaggi precedenti.

#### **Creazione di un numero Diagram**

The following example creates a new diagram from scratch, writes the words "Hello World!" on the first page, and saves the file.

**Crea un nuovo file visio** 

![cose da fare:immagine_alt_testo](your-first-aspose-diagram-application-hello-world_1.png)


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram()

#// Save diagram in the VSDX format
diagram.save("CreateNewVisio_out.vsdx", SaveFileFormat.VSDX)
{{< /highlight >}}


#### **Apertura di un file esistente**

The following example opens an existing Microsoft Visio template file, writes the words "Hello World!" in the first page, and saves the diagram as a new file.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

diagram = Diagram(os.path.join(sourceDir, "Basic Shapes.vss"))

#// Add a new hello world rectangle shape
shapeId = diagram.add_shape(4.25, 5.5, 2, 1, "Rectangle", 0)
shape = diagram.pages[0].shapes.get_shape(shapeId)
shape.text.value.add(Txt("Hello World"))

#// Save diagram in the VSDX format
diagram.save("CreateHelloWorldVisio_out.vsdx", SaveFileFormat.VSDX)
{{< /highlight >}}

