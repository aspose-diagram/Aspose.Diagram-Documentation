---
title: Настройка среды и рекомендации по установке
type: docs
weight: 20
url: /ru/python-java/setup-environment-and-installation-guidelines/
aliases: [/java/aspose-diagram-for-python-via-java-system-requirements/, /pythonjava/system-requirements/]
keywords: python, visio, instal
description: установка Aspose.Diagram для Python через Java и инструкции по установке
---
## **Системные Требования**
 Aspose.Diagram для Python через Java не зависит от платформы API и может использоваться на любой платформе (Windows, Linux и MacOS), где[Python](https://www.python.org/downloads/)установлен. Перед настройкой установки на компьютере должна быть установлена версия Java 8 или выше.

## **Python Версия**
- Python 3,5 или выше
## **Java Версия**
- Java 1,8 или выше

## **Windows:**
### **Установите Java и добавьте его в переменную среды PATH.**
Например:
{{< highlight "java" >}}

PATH=C:\Program Files\Java\jdk1.8.0_131;

{{< /highlight >}}
  
### **Установите Aspose.Diagram для Python через Java с pypi**
 Вы можете легко использовать Aspose.Diagram для Python через Java от[pypi](https://pypi.org/project/aspose-diagram/) с помощью следующей команды.
{{< highlight "java" >}}

 $ pip install aspose-diagram

{{< /highlight >}}

### **Тест Aspose.Diagram для Python через Java**
-  Создайте файл с именем**пример.py**и используйте следующий пример кода:

{{< highlight "java" >}}

import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

diagram = Diagram()
diagram.save("output.vsdx",SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

- Теперь запустите командную строку «python example.py» @, чтобы запустить ее.

## **Линукс:**
### **Установить Java**
  
### **Установите Aspose.Diagram для Python через Java с pypi**
 Вы можете легко использовать Aspose.Diagram для Python через Java от[pypi](https://pypi.org/project/aspose-diagram/) с помощью следующей команды.
{{< highlight "java" >}}

 $ pip install aspose-diagram

{{< /highlight >}}

### **Тест Aspose.Diagram для Python через Java**
-  Создайте файл с именем**пример.py**и используйте следующий пример кода:

{{< highlight "java" >}}

import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

diagram = Diagram()
diagram.save("output.vsdx",SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

- Теперь запустите командную строку «python example.py» @, чтобы запустить ее.

## **макОС:**
### **Установить Java**
  
### **Установите Aspose.Diagram для Python через Java с pypi**
 Вы можете легко использовать Aspose.Diagram для Python через Java от[pypi](https://pypi.org/project/aspose-diagram/) с помощью следующей команды.
{{< highlight "java" >}}

 $ pip install aspose-diagram

{{< /highlight >}}

### **Тест Aspose.Diagram для Python через Java**
-  Создайте файл с именем**пример.py**и используйте следующий пример кода:

{{< highlight "java" >}}

import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

diagram = Diagram()
diagram.save("output.vsdx",SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

- Теперь запустите командную строку «python example.py» @, чтобы запустить ее.

