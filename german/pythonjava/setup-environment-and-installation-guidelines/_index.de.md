---
title: Installationsumgebung und Installationsrichtlinien
type: docs
weight: 20
url: /de/python-java/setup-environment-and-installation-guidelines/
aliases: [/java/aspose-diagram-for-python-via-java-system-requirements/, /pythonjava/system-requirements/]
keywords: python, visio, instal
description: setup Aspose.Diagram for Python via Java and installation guidelines
---
## **System Anforderungen**
Aspose.Diagram for Python via Java is platform-independent API and can be used on any platform (Windows, Linux and MacOS) where [Python](https://www.python.org/downloads/)ist installiert. Die Maschine muss über die Version Java 8 oder höher verfügen, bevor die Installation eingerichtet werden kann.

## **Python-Version**
- Python 3,5 oder höher
## **Java-Version**
- Java 1,8 oder höher

## **Windows:**
### **Installieren Sie Java und fügen Sie es der Umgebungsvariable PATH hinzu**
Zum Beispiel:
{{< highlight "java" >}}

PATH=C:\Program Files\Java\jdk1.8.0_131;

{{< /highlight >}}
  
### **Install Aspose.Diagram for Python via Java from pypi**
You can easily use Aspose.Diagram for Python via Java from [pypi](https://pypi.org/project/aspose-diagram/) mit folgendem Befehl.
{{< highlight "java" >}}

 $ pip install aspose-diagram

{{< /highlight >}}

### **Test Aspose.Diagram for Python via Java**
-  Erstellen Sie eine Datei mit dem Namen**beispiel.py**und verwenden Sie den folgenden Beispielcode:

{{< highlight "java" >}}

import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

diagram = Diagram()
diagram.save("output.vsdx",SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

- Führen Sie nun "python example.py" @command prompt aus, um es auszuführen.

## **Linux:**
### **Installieren Sie Java**
  
### **Install Aspose.Diagram for Python via Java from pypi**
You can easily use Aspose.Diagram for Python via Java from [pypi](https://pypi.org/project/aspose-diagram/) mit folgendem Befehl.
{{< highlight "java" >}}

 $ pip install aspose-diagram

{{< /highlight >}}

### **Test Aspose.Diagram for Python via Java**
-  Erstellen Sie eine Datei mit dem Namen**beispiel.py**und verwenden Sie den folgenden Beispielcode:

{{< highlight "java" >}}

import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

diagram = Diagram()
diagram.save("output.vsdx",SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

- Führen Sie nun "python example.py" @command prompt aus, um es auszuführen.

## **Mac OS:**
### **Installieren Sie Java**
  
### **Install Aspose.Diagram for Python via Java from pypi**
You can easily use Aspose.Diagram for Python via Java from [pypi](https://pypi.org/project/aspose-diagram/) mit folgendem Befehl.
{{< highlight "java" >}}

 $ pip install aspose-diagram

{{< /highlight >}}

### **Test Aspose.Diagram for Python via Java**
-  Erstellen Sie eine Datei mit dem Namen**beispiel.py**und verwenden Sie den folgenden Beispielcode:

{{< highlight "java" >}}

import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

diagram = Diagram()
diagram.save("output.vsdx",SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

- Führen Sie nun "python example.py" @command prompt aus, um es auszuführen.

