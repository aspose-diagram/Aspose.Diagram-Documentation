---
title: Iniziare
linktitle: Iniziare
type: docs
weight: 4
url: /it/python-net/getting-started/ 
keywords: python, visio, instal
description: Setup Aspose.Diagram for Python via .NET and installation guidelines.
---
## **Requisiti di sistema**
Aspose.Diagram for Python via .NET is platform-independent API and can be used on any platform (Windows and Linux) where [Python](https://www.python.org/downloads/) è installato.

## **Python Versione**
- Python 3.6 o superiore

## **Installazione**
### **Windows:**
You can easily use Aspose.Diagram for Python via .NET from [pypi](https://pypi.org/project/aspose-diagram-python/) con il seguente comando.
{{< highlight "NET" >}}

 $ pip install aspose-diagram-python

{{< /highlight >}}

### **Linux:**
You can easily use Aspose.Diagram for Python via .NET from [pypi](https://pypi.org/project/aspose-diagram-python/) con il seguente comando.
{{< highlight "NET" >}}

 $ pip install aspose-diagram-python

{{< /highlight >}}

## **Creating the Hello World Application**

-  Crea un file denominato**Creazione di NewVisioFile.py** e utilizzare il seguente codice di esempio:


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram()

#// Save diagram in the VSDX format
diagram.save("CreateNewVisio_out.vsdx", SaveFileFormat.VSDX)
{{< /highlight >}}


- Ora salva il codice sopra in "CreatingNewVisioFile.py" ed esegui "python CreatingNewVisioFile.py" @command prompt.
