---
title: Empezando
linktitle: Empezando
type: docs
weight: 4
url: /es/python-net/getting-started/ 
keywords: python, visio, instal
description: Setup Aspose.Diagram for Python via .NET and installation guidelines.
---
## **Requisitos del sistema**
Aspose.Diagram for Python via .NET is platform-independent API and can be used on any platform (Windows and Linux) where [Python](https://www.python.org/downloads/) esta instalado.

## **Python Versión**
- Python 3.6 o superior

## **Instalación**
### **Windows:**
You can easily use Aspose.Diagram for Python via .NET from [pypi](https://pypi.org/project/aspose-diagram-python/) con el siguiente comando.
{{< highlight "NET" >}}

 $ pip install aspose-diagram-python

{{< /highlight >}}

### **Linux:**
You can easily use Aspose.Diagram for Python via .NET from [pypi](https://pypi.org/project/aspose-diagram-python/) con el siguiente comando.
{{< highlight "NET" >}}

 $ pip install aspose-diagram-python

{{< /highlight >}}

## **Creating the Hello World Application**

-  Crear un archivo llamado**CreandoNuevoVisioFile.py** y use el siguiente código de muestra:


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram()

#// Save diagram in the VSDX format
diagram.save("CreateNewVisio_out.vsdx", SaveFileFormat.VSDX)
{{< /highlight >}}


- Ahora guarde el código anterior en "CreatingNewVisioFile.py" y ejecute "python CreatingNewVisioFile.py" en el símbolo del sistema.
