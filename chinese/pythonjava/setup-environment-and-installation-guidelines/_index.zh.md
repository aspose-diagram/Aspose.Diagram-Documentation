---
title: 设置环境和安装指南
type: docs
weight: 20
url: /zh/python-java/setup-environment-and-installation-guidelines/
aliases: [/java/aspose-diagram-for-python-via-java-system-requirements/, /pythonjava/system-requirements/]
keywords: python, visio, instal
description: setup Aspose.Diagram for Python via Java and installation guidelines
---
## **系统要求**
Aspose.Diagram for Python via Java is platform-independent API and can be used on any platform (Windows, Linux and MacOS) where [Python](https://www.python.org/downloads/)已安装。在设置安装之前，机器必须具有 Java 8 或更高版本。

## **Python版本**
- Python 3.5 或更高
## **Java版本**
- Java 1.8 或更高版本

## **Windows:**
### **安装Java，加入PATH环境变量**
例如：
{{< highlight "java" >}}

PATH=C:\Program Files\Java\jdk1.8.0_131;

{{< /highlight >}}
  
### **Install Aspose.Diagram for Python via Java from pypi**
You can easily use Aspose.Diagram for Python via Java from [pypi](https://pypi.org/project/aspose-diagram/)使用以下命令。
{{< highlight "java" >}}

 $ pip install aspose-diagram

{{< /highlight >}}

### **Test Aspose.Diagram for Python via Java**
- 创建一个名为**例子.py**并使用以下示例代码：

{{< highlight "java" >}}

import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

diagram = Diagram()
diagram.save("output.vsdx",SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

- 现在运行“python example.py”@命令提示符来运行它。

## **Linux：**
### **安装 Java**
  
### **Install Aspose.Diagram for Python via Java from pypi**
You can easily use Aspose.Diagram for Python via Java from [pypi](https://pypi.org/project/aspose-diagram/)使用以下命令。
{{< highlight "java" >}}

 $ pip install aspose-diagram

{{< /highlight >}}

### **Test Aspose.Diagram for Python via Java**
- 创建一个名为**例子.py**并使用以下示例代码：

{{< highlight "java" >}}

import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

diagram = Diagram()
diagram.save("output.vsdx",SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

- 现在运行“python example.py”@命令提示符来运行它。

## **苹果系统：**
### **安装 Java**
  
### **Install Aspose.Diagram for Python via Java from pypi**
You can easily use Aspose.Diagram for Python via Java from [pypi](https://pypi.org/project/aspose-diagram/)使用以下命令。
{{< highlight "java" >}}

 $ pip install aspose-diagram

{{< /highlight >}}

### **Test Aspose.Diagram for Python via Java**
- 创建一个名为**例子.py**并使用以下示例代码：

{{< highlight "java" >}}

import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

diagram = Diagram()
diagram.save("output.vsdx",SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

- 现在运行“python example.py”@命令提示符来运行它。

