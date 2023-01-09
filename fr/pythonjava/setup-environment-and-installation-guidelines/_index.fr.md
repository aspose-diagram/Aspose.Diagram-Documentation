---
title: Environnement de configuration et directives d'installation
type: docs
weight: 20
url: /fr/python-java/setup-environment-and-installation-guidelines/
aliases: [/java/aspose-diagram-for-python-via-java-system-requirements/, /pythonjava/system-requirements/]
keywords: python, visio, instal
description: setup Aspose.Diagram for Python via Java and installation guidelines
---
## **Configuration requise**
Aspose.Diagram for Python via Java is platform-independent API and can be used on any platform (Windows, Linux and MacOS) where [Python](https://www.python.org/downloads/)est installé. La machine doit disposer des versions Java 8 ou supérieures avant de configurer l'installation.

## **Version Python**
- Python 3.5 ou supérieur
## **Version Java**
- Java 1.8 ou supérieur

## **Windows:**
### **Installez Java et ajoutez-le à la variable d'environnement PATH**
Par exemple:
{{< highlight "java" >}}

PATH=C:\Program Files\Java\jdk1.8.0_131;

{{< /highlight >}}
  
### **Install Aspose.Diagram for Python via Java from pypi**
You can easily use Aspose.Diagram for Python via Java from [pypi](https://pypi.org/project/aspose-diagram/) avec la commande suivante.
{{< highlight "java" >}}

 $ pip install aspose-diagram

{{< /highlight >}}

### **Test Aspose.Diagram for Python via Java**
-  Créer un fichier nommé**exemple.py**et utilisez l'exemple de code suivant :

{{< highlight "java" >}}

import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

diagram = Diagram()
diagram.save("output.vsdx",SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

- Maintenant, lancez "python example.py" @invite de commande pour l'exécuter.

## **Linux :**
### **Installer Java**
  
### **Install Aspose.Diagram for Python via Java from pypi**
You can easily use Aspose.Diagram for Python via Java from [pypi](https://pypi.org/project/aspose-diagram/) avec la commande suivante.
{{< highlight "java" >}}

 $ pip install aspose-diagram

{{< /highlight >}}

### **Test Aspose.Diagram for Python via Java**
-  Créer un fichier nommé**exemple.py**et utilisez l'exemple de code suivant :

{{< highlight "java" >}}

import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

diagram = Diagram()
diagram.save("output.vsdx",SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

- Maintenant, lancez "python example.py" @invite de commande pour l'exécuter.

## **Mac OS :**
### **Installer Java**
  
### **Install Aspose.Diagram for Python via Java from pypi**
You can easily use Aspose.Diagram for Python via Java from [pypi](https://pypi.org/project/aspose-diagram/) avec la commande suivante.
{{< highlight "java" >}}

 $ pip install aspose-diagram

{{< /highlight >}}

### **Test Aspose.Diagram for Python via Java**
-  Créer un fichier nommé**exemple.py**et utilisez l'exemple de code suivant :

{{< highlight "java" >}}

import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

diagram = Diagram()
diagram.save("output.vsdx",SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

- Maintenant, lancez "python example.py" @invite de commande pour l'exécuter.

