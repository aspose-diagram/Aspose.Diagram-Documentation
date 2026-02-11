---
title: Olika sätt att öppna filer
type: docs
weight: 10
url: /sv/python-net/different-ways-to-open-files/
---
{{% alert color="primary" %}}

Med Aspose.Diagram är det enkelt att öppna filer, till exempel för att hämta data, eller att använda en designermall för att påskynda utvecklingsprocessen.

{{% /alert %}}

## **Öppna en fil via en sökväg**

 Utvecklare kan öppna en Microsoft Diagram fil med hjälp av dess sökväg på den lokala datorn genom att ange den i**Diagram**klass konstruktör. Passera helt enkelt vägen i konstruktorn som en*sträng*. Aspose.Diagram kommer automatiskt att upptäcka filformatstypen.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the VSDX format
diagram.save("CreateNewVisio_out.vsdx", SaveFileFormat.VSDX)
{{< /highlight >}}


## **Öppna en fil via a Stream**

 Det är också enkelt att öppna en Visio-fil som en stream. För att göra det, använd en överbelastad version av konstruktorn som tar*BufferStream*objekt som innehåller filen.


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


## **Öppna en fil med LoadOptions**

 För att öppna en fil med laddningsalternativ, använd**LoadOptions**klasser för att ställa in relaterade alternativ för klasserna för mallfilen som ska laddas.


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


