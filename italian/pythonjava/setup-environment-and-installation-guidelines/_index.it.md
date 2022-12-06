---
title: Ambiente di configurazione e linee guida per l'installazione
type: docs
weight: 20
url: /it/python-java/setup-environment-and-installation-guidelines/
aliases: [/java/aspose-diagram-for-python-via-java-system-requirements/, /pythonjava/system-requirements/]
keywords: python, visio, instal
description: setup Aspose.Diagram for Python via Java and installation guidelines
---
## **Requisiti di sistema**
Aspose.Diagram for Python via Java is platform-independent API and can be used on any platform (Windows, Linux and MacOS) where [Python](https://www.python.org/downloads/)è installato. La macchina deve avere Java 8 o versioni successive prima di configurare l'installazione.

## **Python Versione**
- Python 3.5 o superiore
## **Java Versione**
- Java 1.8 o superiore

## **Windows:**
### **Installa Java e aggiungilo alla variabile di ambiente PATH**
Per esempio:
{{< highlight "java" >}}

PATH=C:\Program Files\Java\jdk1.8.0_131;

{{< /highlight >}}
  
### **Install Aspose.Diagram for Python via Java from pypi**
You can easily use Aspose.Diagram for Python via Java from [pypi](https://pypi.org/project/aspose-diagram/) con il seguente comando.
{{< highlight "java" >}}

 $ pip install aspose-diagram

{{< /highlight >}}

### **Test Aspose.Diagram for Python via Java**
-  Crea un file denominato**esempio.py**e utilizzare il seguente codice di esempio:

{{< highlight "java" >}}

import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

diagram = Diagram()
diagram.save("output.vsdx",SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

- Ora esegui "python example.py" @command prompt per eseguirlo.

## **Linux:**
### **Installa Java**
  
### **Install Aspose.Diagram for Python via Java from pypi**
You can easily use Aspose.Diagram for Python via Java from [pypi](https://pypi.org/project/aspose-diagram/) con il seguente comando.
{{< highlight "java" >}}

 $ pip install aspose-diagram

{{< /highlight >}}

### **Test Aspose.Diagram for Python via Java**
-  Crea un file denominato**esempio.py**e utilizzare il seguente codice di esempio:

{{< highlight "java" >}}

import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

diagram = Diagram()
diagram.save("output.vsdx",SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

- Ora esegui "python example.py" @command prompt per eseguirlo.

## **Mac OS:**
### **Installa Java**
  
### **Install Aspose.Diagram for Python via Java from pypi**
You can easily use Aspose.Diagram for Python via Java from [pypi](https://pypi.org/project/aspose-diagram/) con il seguente comando.
{{< highlight "java" >}}

 $ pip install aspose-diagram

{{< /highlight >}}

### **Test Aspose.Diagram for Python via Java**
-  Crea un file denominato**esempio.py**e utilizzare il seguente codice di esempio:

{{< highlight "java" >}}

import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

diagram = Diagram()
diagram.save("output.vsdx",SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

- Ora esegui "python example.py" @command prompt per eseguirlo.

