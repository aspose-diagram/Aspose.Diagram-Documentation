---
title: Diferentes formas de abrir archivos
type: docs
weight: 10
url: /es/python-net/different-ways-to-open-files/
---
{{% alert color="primary" %}}

Con Aspose.Diagram es sencillo abrir archivos, por ejemplo, para recuperar datos o utilizar una plantilla de diseñador para acelerar el proceso de desarrollo.

{{% /alert %}}

## **Opening a File via a Path**

 Los desarrolladores pueden abrir un archivo Microsoft Diagram usando su ruta de archivo en la computadora local especificándolo en el**Diagram**constructor de clases. Simplemente pase la ruta en el constructor como un*cuerda*. Aspose.Diagram detectará automáticamente el tipo de formato de archivo.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the VSDX format
diagram.save("CreateNewVisio_out.vsdx", SaveFileFormat.VSDX)
{{< /highlight >}}


## **Opening a File via a Stream**

 También es sencillo abrir un archivo Visio como flujo. Para hacerlo, use una versión sobrecargada del constructor que toma el*BufferStream*objeto que contiene el archivo.


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


## **Abrir un archivo con LoadOptions**

 Para abrir un archivo con opciones de carga, use el**Opciones de carga**clases para configurar las opciones relacionadas de las clases para que se cargue el archivo de plantilla.


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


