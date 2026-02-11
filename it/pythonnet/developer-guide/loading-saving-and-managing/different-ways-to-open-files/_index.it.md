---
title: Diversi modi per aprire i file
type: docs
weight: 10
url: /it/python-net/different-ways-to-open-files/
---
{{% alert color="primary" %}}

Con Aspose.Diagram è semplice aprire file, ad esempio, per recuperare dati o utilizzare un modello di designer per velocizzare il processo di sviluppo.

{{% /alert %}}

## **Opening a File via a Path**

 Gli sviluppatori possono aprire un file Microsoft Diagram utilizzando il relativo percorso file sul computer locale specificandolo nel**Diagram**costruttore di classe. Basta passare il percorso nel costruttore come a*corda*. Aspose.Diagram rileverà automaticamente il tipo di formato del file.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the VSDX format
diagram.save("CreateNewVisio_out.vsdx", SaveFileFormat.VSDX)
{{< /highlight >}}


## **Opening a File via a Stream**

 È anche semplice aprire un file Visio come flusso. Per fare ciò, usa una versione sovraccaricata del costruttore che accetta il*BufferStream*oggetto che contiene il file.


{{< highlight python >}}
import os
import sys
import aspose.diagram
from aspose.diagram import *
from aspose.pyio import BufferStream

#// Build path of an existing diagram
visioDrawing = os.path.join(sourceDir, "Drawing1.vsdx")
# Create a Stream object
f = open(visioDrawing, 'rb')
data = f.read()
databuff = BufferStream(data)
diagram = Diagram(databuff)

#// Save diagram in the VSDX format
diagram.save("Visio_out.vsdx", SaveFileFormat.VSDX)
{{< /highlight >}}


## **Apertura di un file con LoadOptions**

 Per aprire un file con opzioni di caricamento, utilizzare il file**LoadOptions**classes per impostare le opzioni correlate delle classi per il file modello da caricare.


{{< highlight python >}}
import os
import sys
import aspose.diagram
from aspose.diagram import *

#// Build path of an existing diagram
visioDrawing = os.path.join(sourceDir, "Drawing1.vsdx")
# Instantiate LoadOptions specified by the LoadFileFormat
loadOptions = LoadOptions(LoadFileFormat.VSDX)
diagram = Diagram(visioDrawing,loadOptions)

#// Save diagram in the VSDX format
diagram.save("Visio_out.vsdx", SaveFileFormat.VSDX)
{{< /highlight >}}


