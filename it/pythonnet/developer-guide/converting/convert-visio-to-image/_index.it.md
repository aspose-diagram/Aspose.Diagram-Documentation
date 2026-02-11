---
title:  Converti Visio in formati Immagini
linktitle: Converti Visio in immagini
type: docs
weight: 20
url: /it/python-net/convert-visio-to-image/
description: This topic show you how to Aspose.Diagram allows to convert Visio to various images formats. Convert Visio,VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to PNG, JPEG, BMP images with a few lines of code.
---
## **Esporta diagrammi in formati di file immagine**
 Questo articolo spiega come esportare un Microsoft Visio diagram in un'immagine utilizzando[Aspose.Diagram for .NET](https://products.aspose.com/diagram/python-net/) API. Utilizzare il costruttore della classe [Diagram] per leggere i file diagram e il metodo Save per esportare diagram in qualsiasi formato di immagine supportato.

Per esportare un diagram in un'immagine:

- Creare un'istanza della classe Diagram.
- Chiama il metodo Save della classe Diagram e imposta il formato dell'immagine in cui desideri esportare. Il file dell'immagine di output ha l'aspetto del file originale.
### **Esporta Microsoft Visio Disegno su file immagine**

{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the png format
diagram.save("Visio_out.png", SaveFileFormat.PNG)
{{< /highlight >}}


È anche possibile salvare una pagina particolare come immagine, invece dell'intero documento:


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))
#// Save diagram as PNG
options = saving.ImageSaveOptions(SaveFileFormat.PNG)
    
#// Save one page only, by page index
options.page_index = 0

#// Save diagram in the png format
diagram.save("ExportPageToImage_out.png", options)
{{< /highlight >}}
