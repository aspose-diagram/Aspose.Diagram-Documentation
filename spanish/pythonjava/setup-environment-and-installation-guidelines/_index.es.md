---
title: Entorno de configuración y pautas de instalación
type: docs
weight: 20
url: /es/python-java/setup-environment-and-installation-guidelines/
aliases: [/java/aspose-diagram-for-python-via-java-system-requirements/, /pythonjava/system-requirements/]
keywords: python, visio, instal
description: setup Aspose.Diagram for Python via Java and installation guidelines
---
## **Requisitos del sistema**
Aspose.Diagram for Python via Java is platform-independent API and can be used on any platform (Windows, Linux and MacOS) where [Python](https://www.python.org/downloads/)esta instalado. La máquina debe tener Java 8 o versiones superiores antes de configurar la instalación.

## **Python Versión**
- Python 3.5 o superior
## **Java Versión**
- Java 1.8 o superior

## **Windows:**
### **Instale Java y agréguelo a la variable de entorno PATH**
Por ejemplo:
{{< highlight "java" >}}

PATH=C:\Program Files\Java\jdk1.8.0_131;

{{< /highlight >}}
  
### **Install Aspose.Diagram for Python via Java from pypi**
You can easily use Aspose.Diagram for Python via Java from [pypi](https://pypi.org/project/aspose-diagram/) con el siguiente comando.
{{< highlight "java" >}}

 $ pip install aspose-diagram

{{< /highlight >}}

### **Test Aspose.Diagram for Python via Java**
-  Crear un archivo llamado**ejemplo.py**y use el siguiente código de ejemplo:

{{< highlight "java" >}}

import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

diagram = Diagram()
diagram.save("output.vsdx",SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

- Ahora ejecute "python example.py" @ símbolo del sistema para ejecutarlo.

## **Linux:**
### **Instalar Java**
  
### **Install Aspose.Diagram for Python via Java from pypi**
You can easily use Aspose.Diagram for Python via Java from [pypi](https://pypi.org/project/aspose-diagram/) con el siguiente comando.
{{< highlight "java" >}}

 $ pip install aspose-diagram

{{< /highlight >}}

### **Test Aspose.Diagram for Python via Java**
-  Crear un archivo llamado**ejemplo.py**y use el siguiente código de ejemplo:

{{< highlight "java" >}}

import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

diagram = Diagram()
diagram.save("output.vsdx",SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

- Ahora ejecute "python example.py" @ símbolo del sistema para ejecutarlo.

## **Mac OS:**
### **Instalar Java**
  
### **Install Aspose.Diagram for Python via Java from pypi**
You can easily use Aspose.Diagram for Python via Java from [pypi](https://pypi.org/project/aspose-diagram/) con el siguiente comando.
{{< highlight "java" >}}

 $ pip install aspose-diagram

{{< /highlight >}}

### **Test Aspose.Diagram for Python via Java**
-  Crear un archivo llamado**ejemplo.py**y use el siguiente código de ejemplo:

{{< highlight "java" >}}

import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

diagram = Diagram()
diagram.save("output.vsdx",SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

- Ahora ejecute "python example.py" @ símbolo del sistema para ejecutarlo.

