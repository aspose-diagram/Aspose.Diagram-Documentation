---
title:  Convertir Visio en formats Images
linktitle: Convertir Visio en Images
type: docs
weight: 20
url: /fr/python-net/convert-visio-to-image/
description: This topic show you how to Aspose.Diagram allows to convert Visio to various images formats. Convert Visio,VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to PNG, JPEG, BMP images with a few lines of code.
---
## **Exporter des diagrammes vers des formats de fichier image**
 Cet article explique comment exporter un Microsoft Visio diagram vers une image en utilisant[Aspose.Diagram for .NET](https://products.aspose.com/diagram/python-net/) API. Utilisez le constructeur de classe [Diagram] pour lire les fichiers diagram et la méthode Save pour exporter le diagram vers n'importe quel format d'image pris en charge.

Pour exporter un diagram vers une image :

- Créez une instance de la classe Diagram.
- Appelez la méthode Save de la classe Diagram et définissez le format d'image vers lequel vous souhaitez exporter. Le fichier image de sortie ressemble au fichier d'origine.
### **Exporter Microsoft Visio Dessin vers un fichier image**

{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the png format
diagram.save("Visio_out.png", SaveFileFormat.PNG)
{{< /highlight >}}


Il est également possible d'enregistrer une page particulière dans l'image, au lieu du document entier :


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
