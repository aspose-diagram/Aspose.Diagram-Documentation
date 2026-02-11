---
title: Einstieg
linktitle: Einstieg
type: docs
weight: 4
url: /de/python-net/getting-started/ 
keywords: python, visio, instal
description: Setup Aspose.Diagram for Python via .NET and installation guidelines.
---
## **System Anforderungen**
Aspose.Diagram for Python via .NET is platform-independent API and can be used on any platform (Windows and Linux) where [Python](https://www.python.org/downloads/) ist installiert.

## **Python-Version**
- Python 3,6 oder höher

## **Installation**
### **Windows:**
You can easily use Aspose.Diagram for Python via .NET from [pypi](https://pypi.org/project/aspose-diagram-python/) mit folgendem Befehl.
{{< highlight "NET" >}}

 $ pip install aspose-diagram-python

{{< /highlight >}}

### **Linux:**
You can easily use Aspose.Diagram for Python via .NET from [pypi](https://pypi.org/project/aspose-diagram-python/) mit folgendem Befehl.
{{< highlight "NET" >}}

 $ pip install aspose-diagram-python

{{< /highlight >}}

## **Creating the Hello World Application**

-  Erstellen Sie eine Datei mit dem Namen**Erstellen von NewVisioFile.py** und verwenden Sie den folgenden Beispielcode:


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram()

#// Save diagram in the VSDX format
diagram.save("CreateNewVisio_out.vsdx", SaveFileFormat.VSDX)
{{< /highlight >}}


- Speichern Sie nun den obigen Code in „CreatingNewVisioFile.py“ und führen Sie „python CreatingNewVisioFile.py“ @command prompt aus.
