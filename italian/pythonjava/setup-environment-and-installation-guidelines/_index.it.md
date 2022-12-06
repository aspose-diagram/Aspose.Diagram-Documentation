---
title: Ambiente di configurazione e linee guida per l'installazione
type: docs
weight: 20
url: /it/python-java/setup-environment-and-installation-guidelines/
aliases: [/java/aspose-diagram-for-python-via-java-system-requirements/, /pythonjava/system-requirements/]
keywords: python, visio, instal
description: configurazione Aspose.Diagram per Python tramite Java e linee guida per l'installazione
---
## **Requisiti di sistema**
 Aspose.Diagram per Python tramite Java è indipendente dalla piattaforma API e può essere utilizzato su qualsiasi piattaforma (Windows, Linux e MacOS) dove[Python](https://www.python.org/downloads/)è installato. La macchina deve avere Java 8 o versioni successive prima di configurare l'installazione.

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
  
### **Installa Aspose.Diagram per Python tramite Java da pypi**
 Puoi facilmente utilizzare Aspose.Diagram per Python tramite Java da[pypi](https://pypi.org/project/aspose-diagram/) con il seguente comando.
{{< highlight "java" >}}

 $ pip install aspose-diagram

{{< /highlight >}}

### **Prova Aspose.Diagram per Python tramite Java**
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
  
### **Installa Aspose.Diagram per Python tramite Java da pypi**
 Puoi facilmente utilizzare Aspose.Diagram per Python tramite Java da[pypi](https://pypi.org/project/aspose-diagram/) con il seguente comando.
{{< highlight "java" >}}

 $ pip install aspose-diagram

{{< /highlight >}}

### **Prova Aspose.Diagram per Python tramite Java**
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
  
### **Installa Aspose.Diagram per Python tramite Java da pypi**
 Puoi facilmente utilizzare Aspose.Diagram per Python tramite Java da[pypi](https://pypi.org/project/aspose-diagram/) con il seguente comando.
{{< highlight "java" >}}

 $ pip install aspose-diagram

{{< /highlight >}}

### **Prova Aspose.Diagram per Python tramite Java**
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

