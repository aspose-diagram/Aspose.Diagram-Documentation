---
title: 设置环境和安装指南
type: docs
weight: 20
url: /zh/python-java/setup-environment-and-installation-guidelines/
aliases: [/java/aspose-diagram-for-python-via-java-system-requirements/, /pythonjava/system-requirements/]
keywords: python, visio, instal
description: 通过 Java 为 Python 设置 Aspose.Diagram 和安装指南
---
## **系统要求**
 Aspose.Diagram for Python via Java 与平台无关 API 可以在任何平台（Windows，Linux 和 MacOS）上使用，其中[Python](https://www.python.org/downloads/)已安装。在设置安装之前，机器必须具有 Java 8 或更高版本。

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
  
### **从 pypi 通过 Java 为 Python 安装 Aspose.Diagram**
您可以通过 Java 轻松地将 Aspose.Diagram 用于 Python 来自[pypi](https://pypi.org/project/aspose-diagram/)使用以下命令。
{{< highlight "java" >}}

 $ pip install aspose-diagram

{{< /highlight >}}

### **通过 Java 测试 Aspose.Diagram 为 Python**
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
  
### **从 pypi 通过 Java 为 Python 安装 Aspose.Diagram**
您可以通过 Java 轻松地将 Aspose.Diagram 用于 Python 来自[pypi](https://pypi.org/project/aspose-diagram/)使用以下命令。
{{< highlight "java" >}}

 $ pip install aspose-diagram

{{< /highlight >}}

### **通过 Java 测试 Aspose.Diagram 为 Python**
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
  
### **从 pypi 通过 Java 为 Python 安装 Aspose.Diagram**
您可以通过 Java 轻松地将 Aspose.Diagram 用于 Python 来自[pypi](https://pypi.org/project/aspose-diagram/)使用以下命令。
{{< highlight "java" >}}

 $ pip install aspose-diagram

{{< /highlight >}}

### **通过 Java 测试 Aspose.Diagram 为 Python**
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

