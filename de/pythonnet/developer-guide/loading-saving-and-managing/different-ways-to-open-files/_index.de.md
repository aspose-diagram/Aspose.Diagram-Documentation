---
title: Verschiedene Möglichkeiten zum Öffnen von Dateien
type: docs
weight: 10
url: /de/python-net/different-ways-to-open-files/
---
{{% alert color="primary" %}}

Mit Aspose.Diagram ist es beispielsweise einfach, Dateien zu öffnen, Daten abzurufen oder eine Designer-Vorlage zu verwenden, um den Entwicklungsprozess zu beschleunigen.

{{% /alert %}}

## **Opening a File via a Path**

 Entwickler können eine Microsoft Diagram-Datei öffnen, indem sie ihren Dateipfad auf dem lokalen Computer verwenden, indem sie ihn in der**Diagram**Klassenkonstrukteur. Übergeben Sie den Pfad einfach im Konstruktor als a*Schnur*. Aspose.Diagram erkennt automatisch den Dateiformattyp.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the VSDX format
diagram.save("CreateNewVisio_out.vsdx", SaveFileFormat.VSDX)
{{< /highlight >}}


## **Opening a File via a Stream**

 Es ist auch einfach, eine Visio-Datei als Stream zu öffnen. Verwenden Sie dazu eine überladene Version des Konstruktors, der die akzeptiert*BufferStream*Objekt, das die Datei enthält.


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


## **Öffnen einer Datei mit LoadOptions**

 Um eine Datei mit Ladeoptionen zu öffnen, verwenden Sie die**Ladeoptionen**Klassen, um die zugehörigen Optionen der Klassen für die zu ladende Vorlagendatei festzulegen.


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


