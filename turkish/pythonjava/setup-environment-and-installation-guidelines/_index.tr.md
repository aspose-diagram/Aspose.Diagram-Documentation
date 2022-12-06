---
title: Kurulum Ortamı ve Kurulum Yönergeleri
type: docs
weight: 20
url: /tr/python-java/setup-environment-and-installation-guidelines/
aliases: [/java/aspose-diagram-for-python-via-java-system-requirements/, /pythonjava/system-requirements/]
keywords: python, visio, instal
description: setup Aspose.Diagram for Python via Java and installation guidelines
---
## **sistem gereksinimleri**
 Java üzerinden Python için Aspose.Diagram, platformdan bağımsız API'dir ve herhangi bir platformda (Windows, Linux ve MacOS) kullanılabilir.[Python](https://www.python.org/downloads/)kurulur. Kurulum yapılmadan önce makinenin Java 8 veya üzeri sürümleri olmalıdır.

## **Python Versiyon**
- Python 3.5 veya üstü
## **Java Versiyon**
- Java 1.8 veya üstü

## **Windows:**
### **Java'i yükleyin ve PATH ortam değişkenine ekleyin**
Örneğin:
{{< highlight "java" >}}

PATH=C:\Program Files\Java\jdk1.8.0_131;

{{< /highlight >}}
  
### **pypi'den Java aracılığıyla Python için Aspose.Diagram'i kurun**
 Java üzerinden Python için Aspose.Diagram'i rahatlıkla kullanabilirsiniz.[pypi](https://pypi.org/project/aspose-diagram/) aşağıdaki komutla.
{{< highlight "java" >}}

 $ pip install aspose-diagram

{{< /highlight >}}

### **Java aracılığıyla Python için Aspose.Diagram'i test edin**
-  adlı bir dosya oluşturun.**örnek.py**ve aşağıdaki örnek kodu kullanın:

{{< highlight "java" >}}

import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

diagram = Diagram()
diagram.save("output.vsdx",SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

- Şimdi çalıştırmak için "python example.py" @command istemini çalıştırın.

## **Linux:**
### **Java'i yükleyin**
  
### **pypi'den Java aracılığıyla Python için Aspose.Diagram'i kurun**
 Java üzerinden Python için Aspose.Diagram'i rahatlıkla kullanabilirsiniz.[pypi](https://pypi.org/project/aspose-diagram/) aşağıdaki komutla.
{{< highlight "java" >}}

 $ pip install aspose-diagram

{{< /highlight >}}

### **Java aracılığıyla Python için Aspose.Diagram'i test edin**
-  adlı bir dosya oluşturun.**örnek.py**ve aşağıdaki örnek kodu kullanın:

{{< highlight "java" >}}

import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

diagram = Diagram()
diagram.save("output.vsdx",SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

- Şimdi çalıştırmak için "python example.py" @command istemini çalıştırın.

## **Mac os işletim sistemi:**
### **Java'i yükleyin**
  
### **pypi'den Java aracılığıyla Python için Aspose.Diagram'i kurun**
 Java üzerinden Python için Aspose.Diagram'i rahatlıkla kullanabilirsiniz.[pypi](https://pypi.org/project/aspose-diagram/) aşağıdaki komutla.
{{< highlight "java" >}}

 $ pip install aspose-diagram

{{< /highlight >}}

### **Java aracılığıyla Python için Aspose.Diagram'i test edin**
-  adlı bir dosya oluşturun.**örnek.py**ve aşağıdaki örnek kodu kullanın:

{{< highlight "java" >}}

import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

diagram = Diagram()
diagram.save("output.vsdx",SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

- Şimdi çalıştırmak için "python example.py" @command istemini çalıştırın.

