---
title: Environnement de configuration et directives d'installation
type: docs
weight: 20
url: /fr/python-java/setup-environment-and-installation-guidelines/
aliases: [/java/aspose-diagram-for-python-via-java-system-requirements/, /pythonjava/system-requirements/]
keywords: python, visio, instal
description: configuration Aspose.Diagram pour Python via Java et directives d'installation
---
## **Configuration requise**
 Aspose.Diagram pour Python via Java est indépendant de la plate-forme API et peut être utilisé sur n'importe quelle plate-forme (Windows, Linux et MacOS) où[Python](https://www.python.org/downloads/)est installé. La machine doit disposer des versions Java 8 ou supérieures avant de configurer l'installation.

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
  
### **Installez Aspose.Diagram pour Python via Java à partir de pypi**
 Vous pouvez facilement utiliser Aspose.Diagram pour Python via Java à partir de[pypi](https://pypi.org/project/aspose-diagram/) avec la commande suivante.
{{< highlight "java" >}}

 $ pip install aspose-diagram

{{< /highlight >}}

### **Testez Aspose.Diagram pour Python via Java**
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
  
### **Installez Aspose.Diagram pour Python via Java à partir de pypi**
 Vous pouvez facilement utiliser Aspose.Diagram pour Python via Java à partir de[pypi](https://pypi.org/project/aspose-diagram/) avec la commande suivante.
{{< highlight "java" >}}

 $ pip install aspose-diagram

{{< /highlight >}}

### **Testez Aspose.Diagram pour Python via Java**
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
  
### **Installez Aspose.Diagram pour Python via Java à partir de pypi**
 Vous pouvez facilement utiliser Aspose.Diagram pour Python via Java à partir de[pypi](https://pypi.org/project/aspose-diagram/) avec la commande suivante.
{{< highlight "java" >}}

 $ pip install aspose-diagram

{{< /highlight >}}

### **Testez Aspose.Diagram pour Python via Java**
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

