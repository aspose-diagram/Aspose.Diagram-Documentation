---
title: Komma igång
linktitle: Komma igång
type: docs
weight: 4
url: /sv/python-net/getting-started/ 
keywords: python, visio, instal
description: Ställ in Aspose.Diagram för Python via .NET och installationsriktlinjer.
---
## **Systemkrav**
 Aspose.Diagram för Python via .NET är plattformsoberoende API och kan användas på alla plattformar (Windows och Linux) där[Python](https://www.python.org/downloads/) är installerad.

## **Python Version**
- Python 3.6 eller högre

## **Installation**
### **Windows:**
 Du kan enkelt använda Aspose.Diagram för Python via .NET från[pypi](https://pypi.org/project/aspose-diagram-python/) med följande kommando.
{{< highlight "NET" >}}

 $ pip install aspose-diagram-python

{{< /highlight >}}

### **Linux:**
 Du kan enkelt använda Aspose.Diagram för Python via .NET från[pypi](https://pypi.org/project/aspose-diagram-python/) med följande kommando.
{{< highlight "NET" >}}

 $ pip install aspose-diagram-python

{{< /highlight >}}

## **Skapar Hello World-applikationen**

-  Skapa en fil med namnet**SkaparNewVisioFile.py** och använd följande exempelkod:


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram()

#// Save diagram in the VSDX format
diagram.save("CreateNewVisio_out.vsdx", SaveFileFormat.VSDX)
{{< /highlight >}}


- Spara nu koden ovan till "CreatingNewVisioFile.py" och kör "python CreatingNewVisioFile.py" @kommandotolken.
