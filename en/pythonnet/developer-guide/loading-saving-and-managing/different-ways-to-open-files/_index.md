---
title: Different Ways to Open Files
type: docs
weight: 10
url: /python-net/different-ways-to-open-files/
---

{{% alert color="primary" %}}

With Aspose.Diagram it is simple to open files, for example, to retrieve data, or to use a designer template to speed up the development process.

{{% /alert %}}

## **Opening a File via a Path**

Developers can open a Microsoft Diagram file using its file path on the local computer by specifying it in the **Diagram** class constructor. Simply pass the path in the constructor as a *string*. Aspose.Diagram will automatically detect the file format type.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the VSDX format
diagram.save("CreateNewVisio_out.vsdx", SaveFileFormat.VSDX)
{{< /highlight >}}


## **Opening a File via a Stream**

It is also simple to open an Visio file as a stream. To do so, use an overloaded version of the constructor that takes the *BufferStream* object that contains the file.


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


## **Opening a File with LoadOptions**

To open a file with loadoptions, use the **LoadOptions** classes to set the related options of the classes for the template file to be loaded.


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


