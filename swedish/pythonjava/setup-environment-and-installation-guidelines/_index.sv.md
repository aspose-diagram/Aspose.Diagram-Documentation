---
title: Installationsmiljö och installationsriktlinjer
type: docs
weight: 20
url: /sv/python-java/setup-environment-and-installation-guidelines/
aliases: [/java/aspose-diagram-for-python-via-java-system-requirements/, /pythonjava/system-requirements/]
keywords: python, visio, instal
description: ställ in Aspose.Diagram för Python via Java och installationsriktlinjer
---
## **Systemkrav**
 Aspose.Diagram för Python via Java är plattformsoberoende API och kan användas på alla plattformar (Windows, Linux och MacOS) där[Python](https://www.python.org/downloads/)är installerad. Maskinen måste ha Java 8 eller senare versioner innan installationen ställs in.

## **Python Version**
- Python 3,5 eller högre
## **Java Version**
- Java 1,8 eller högre

## **Windows:**
### **Installera Java och lägg till den i PATH miljövariabel**
Till exempel:
{{< highlight "java" >}}

PATH=C:\Program Files\Java\jdk1.8.0_131;

{{< /highlight >}}
  
### **Installera Aspose.Diagram för Python via Java från pypi**
 Du kan enkelt använda Aspose.Diagram för Python via Java från[pypi](https://pypi.org/project/aspose-diagram/) med följande kommando.
{{< highlight "java" >}}

 $ pip install aspose-diagram

{{< /highlight >}}

### **Testa Aspose.Diagram för Python via Java**
-  Skapa en fil med namnet**exempel.py**och använd följande exempelkod:

{{< highlight "java" >}}

import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

diagram = Diagram()
diagram.save("output.vsdx",SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

- Kör nu "python example.py" @command prompt för att köra det.

## **Linux:**
### **Installera Java**
  
### **Installera Aspose.Diagram för Python via Java från pypi**
 Du kan enkelt använda Aspose.Diagram för Python via Java från[pypi](https://pypi.org/project/aspose-diagram/) med följande kommando.
{{< highlight "java" >}}

 $ pip install aspose-diagram

{{< /highlight >}}

### **Testa Aspose.Diagram för Python via Java**
-  Skapa en fil med namnet**exempel.py**och använd följande exempelkod:

{{< highlight "java" >}}

import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

diagram = Diagram()
diagram.save("output.vsdx",SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

- Kör nu "python example.py" @command prompt för att köra det.

## **Mac OS:**
### **Installera Java**
  
### **Installera Aspose.Diagram för Python via Java från pypi**
 Du kan enkelt använda Aspose.Diagram för Python via Java från[pypi](https://pypi.org/project/aspose-diagram/) med följande kommando.
{{< highlight "java" >}}

 $ pip install aspose-diagram

{{< /highlight >}}

### **Testa Aspose.Diagram för Python via Java**
-  Skapa en fil med namnet**exempel.py**och använd följande exempelkod:

{{< highlight "java" >}}

import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

diagram = Diagram()
diagram.save("output.vsdx",SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

- Kör nu "python example.py" @command prompt för att köra det.

