---
title: Setup Environment and Installation Guidelines
type: docs
weight: 20
url: /pythonjava/setup-environment-and-installation-guidelines/
aliases: [/java/aspose-diagram-for-python-via-java-system-requirements/, /pythonjava/system-requirements/]
keywords: "python, visio, install"
description: "setup Aspose.Diagram for Python via Java and installation guidelines."
---

## **System Requirements**
Aspose.Diagram for Python via Java is platform-independent API and can be used on any platform (Windows, Linux and MacOS) where [Python](https://www.python.org/downloads/) is installed. The machine must have Java 8 or greater versions before setting up the installation.

## **Python Version**
- Python 3.5 or higher
## **Java Version**
- Java 1.8 or higher

## **Windows:**
### **Install Java and add it to PATH environment variable**
For example:
{{< highlight java >}}

PATH=C:\Program Files\Java\jdk1.8.0_131;

{{< /highlight >}}
  
### **Install Aspose.Diagram for Python via Java from pypi**
You can easily use Aspose.Diagram for Python via Java from [pypi](https://pypi.org/project/aspose-diagram/) with the following command.
{{< highlight java >}}

 $ pip install aspose-diagram

{{< /highlight >}}

### **Test Aspose.Diagram for Python via Java**
- Create a file named **example.py** and use the following sample code:

{{< highlight java >}}

import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

diagram = Diagram()
diagram.save("output.vsdx",SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

- Now run "python example.py" @command prompt to run it.

## **Linux:**
### **Install Java**
  
### **Install Aspose.Diagram for Python via Java from pypi**
You can easily use Aspose.Diagram for Python via Java from [pypi](https://pypi.org/project/aspose-diagram/) with the following command.
{{< highlight java >}}

 $ pip install aspose-diagram

{{< /highlight >}}

### **Test Aspose.Diagram for Python via Java**
- Create a file named **example.py** and use the following sample code:

{{< highlight java >}}

import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

diagram = Diagram()
diagram.save("output.vsdx",SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

- Now run "python example.py" @command prompt to run it.

## **macOS:**
### **Install Java**
  
### **Install Aspose.Diagram for Python via Java from pypi**
You can easily use Aspose.Diagram for Python via Java from [pypi](https://pypi.org/project/aspose-diagram/) with the following command.
{{< highlight java >}}

 $ pip install aspose-diagram

{{< /highlight >}}

### **Test Aspose.Diagram for Python via Java**
- Create a file named **example.py** and use the following sample code:

{{< highlight java >}}

import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

diagram = Diagram()
diagram.save("output.vsdx",SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

- Now run "python example.py" @command prompt to run it.

