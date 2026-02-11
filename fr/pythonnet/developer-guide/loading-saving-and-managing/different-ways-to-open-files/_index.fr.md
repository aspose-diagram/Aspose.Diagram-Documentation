---
title: Différentes façons d'ouvrir des fichiers
type: docs
weight: 10
url: /fr/python-net/different-ways-to-open-files/
---
{{% alert color="primary" %}}

Avec Aspose.Diagram, il est simple d'ouvrir des fichiers, par exemple pour récupérer des données, ou d'utiliser un modèle de concepteur pour accélérer le processus de développement.

{{% /alert %}}

## **Opening a File via a Path**

 Les développeurs peuvent ouvrir un fichier Microsoft Diagram en utilisant son chemin de fichier sur l'ordinateur local en le spécifiant dans le**Diagram**constructeur de classe. Passez simplement le chemin dans le constructeur en tant que*chaîne de caractères*. Aspose.Diagram détectera automatiquement le type de format de fichier.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the VSDX format
diagram.save("CreateNewVisio_out.vsdx", SaveFileFormat.VSDX)
{{< /highlight >}}


## **Opening a File via a Stream**

 Il est également simple d'ouvrir un fichier Visio en tant que flux. Pour ce faire, utilisez une version surchargée du constructeur qui prend le*BufferStream*objet qui contient le fichier.


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


## **Ouvrir un fichier avec LoadOptions**

 Pour ouvrir un fichier avec loadoptions, utilisez le**ChargerOptions**classes pour définir les options associées des classes pour le fichier modèle à charger.


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


