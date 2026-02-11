---
title: Your First Aspose.Diagram Application - Hello World
type: docs
weight: 30
url: /it/python-java/your-first-aspose-diagram-application-hello-world/
description: Questa pagina descrive come creare la prima applicazione con la libreria Aspose.Diagram.
---
{{% alert color="primary" %}}

This tutorial shows how to create a very first application (Hello World) using Aspose.Diagram' simple API. This simple application creates a Microsoft Visio file with the text 'Hello World' in a specified Page.

{{% /alert %}}

## **Creating the Hello World Application**

The steps below creates the Hello World application using the Aspose.Diagram API:

1. Creare un'istanza della classe Diagram.
1. Applica la licenza:
 1. Se hai acquistato una licenza, usa la licenza nella tua applicazione per ottenere l'accesso alla piena funzionalità di Aspose.Diagram
 1. Se stai utilizzando la versione di valutazione del componente (se stai utilizzando Aspose.Diagram senza licenza), salta questo passaggio.
1. Crea un nuovo file Visio o apri un file Visio esistente.
1. Crea una nuova casella di testo.
1.  Inserisci le parole**Hello World!** in una casella di testo.
1. Generare il file Microsoft Visio modificato.

L'implementazione dei passaggi precedenti è dimostrata negli esempi seguenti.

### **Code Sample: Creating a New Diagram and Writing Hello World!**

L'esempio seguente apre un file modello Microsoft Visio esistente denominato "[Basic_Shapes.vss](Basic_Shapes.vss)", inputs "Hello World!" text in the first page and saves the diagram.


{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

diagram = Diagram("Basic_Shapes.vss")

# Add a new hello world rectangle shape
shapeId = diagram.addShape(4.25, 5.5, 2, 1, "Rectangle", 0)
shape = diagram.getPages().getPage(0).getShapes().getShape(shapeId)
shape.getText().getValue().add(Txt("Hello World"))

# Save diagram in the VSDX format
diagram.save("CreateHelloWorldVisio_out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

