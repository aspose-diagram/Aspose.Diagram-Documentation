---
title: Minska filstorleken
type: docs
weight: 50
url: /sv/python-java/reduce-file-size/
description: Det här avsnittet förklarar hur du minskar filstorleken från en diagram med Aspose.Diagram för Python via Java.
---
## **Minska filstorleken**
 Aspose.Diagram för Python via Java API tillåter utvecklare att ta bort dold information från en diagram för att minska filstorleken.
 Sidobjektet representerar ritytan på en förgrundssida eller en bakgrundssida. För att minska filstorleken kan du använda egenskaperna RemoveHiddenInfoItem i**RemoveHiddenInformation()** metod av Diagram klass. Kodexemplet nedan visar hur du tar bort dold information från diagram.


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

