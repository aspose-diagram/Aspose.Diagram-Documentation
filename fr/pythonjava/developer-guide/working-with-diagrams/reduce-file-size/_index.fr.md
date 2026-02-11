---
title: Réduire la taille du fichier
type: docs
weight: 50
url: /fr/python-java/reduce-file-size/
description: This section explains how to reduce file size from a diagram with Aspose.Diagram for Python via Java.
---
## **Réduire la taille du fichier**
Aspose.Diagram for Python via Java API allows developers to remove hidden info from a diagram to reduce file size. 
 L'objet Page représente la zone de dessin d'une page de premier plan ou d'une page d'arrière-plan. Afin de réduire la taille du fichier, vous pouvez utiliser les propriétés RemoveHiddenInfoItem dans**Supprimer les informations cachées ()** méthode de la classe Diagram. L'exemple de code ci-dessous montre comment supprimer les informations masquées de diagram.


{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Load a Visio diagram
diagram = Diagram("Drawing1.vsdx")

# Remove hidden information from diagram
diagram.removeHiddenInformation(RemoveHiddenInfoItem.SHAPES | RemoveHiddenInfoItem.MASTERS)

# save in the VSDX format
diagram.save("ReduceFileSize_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

