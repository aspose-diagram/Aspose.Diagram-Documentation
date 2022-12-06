---
title: Kurulum Ortamı ve Kurulum Yönergeleri
type: docs
weight: 20
url: /tr/python-java/setup-environment-and-installation-guidelines/
aliases: [/java/aspose-diagram-for-python-via-java-system-requirements/, /pythonjava/system-requirements/]
keywords: python, visio, instal
description: Python via Java için kurulum Aspose.Diagram ve kurulum yönergeleri
---
## **sistem gereksinimleri**
 Python via Java için Aspose.Diagram, platformdan bağımsızdır API ve herhangi bir platformda (Windows, Linux ve MacOS) kullanılabilir.[Python](https://www.python.org/downloads/)kurulur. Kurulum yapılmadan önce makinenin Java 8 veya üzeri sürümleri olmalıdır.

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
  
### **Aspose.Diagram'i pypi'den Python via Java için yükleyin**
 Python via Java için Aspose.Diagram den rahatlıkla kullanabilirsiniz.[pypi](https://pypi.org/project/aspose-diagram/) aşağıdaki komutla.
{{< highlight "java" >}}

 $ pip install aspose-diagram

{{< /highlight >}}

### **Python via Java için Aspose.Diagram testi**
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
  
### **Aspose.Diagram'i pypi'den Python via Java için yükleyin**
 Python via Java için Aspose.Diagram den rahatlıkla kullanabilirsiniz.[pypi](https://pypi.org/project/aspose-diagram/) aşağıdaki komutla.
{{< highlight "java" >}}

 $ pip install aspose-diagram

{{< /highlight >}}

### **Python via Java için Aspose.Diagram testi**
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
  
### **Aspose.Diagram'i pypi'den Python via Java için yükleyin**
 Python via Java için Aspose.Diagram den rahatlıkla kullanabilirsiniz.[pypi](https://pypi.org/project/aspose-diagram/) aşağıdaki komutla.
{{< highlight "java" >}}

 $ pip install aspose-diagram

{{< /highlight >}}

### **Python via Java için Aspose.Diagram testi**
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

