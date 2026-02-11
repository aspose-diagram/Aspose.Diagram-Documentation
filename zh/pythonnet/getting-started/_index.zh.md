---
title: 入门
linktitle: 入门
type: docs
weight: 4
url: /zh/python-net/getting-started/ 
keywords: python, visio, instal
description: Setup Aspose.Diagram for Python via .NET and installation guidelines.
---
## **系统要求**
Aspose.Diagram for Python via .NET is platform-independent API and can be used on any platform (Windows and Linux) where [Python](https://www.python.org/downloads/)已安装。

## **Python版本**
- Python 3.6 或更高版本

## **安装**
### **Windows:**
You can easily use Aspose.Diagram for Python via .NET from [pypi](https://pypi.org/project/aspose-diagram-python/)使用以下命令。
{{< highlight "NET" >}}

 $ pip install aspose-diagram-python

{{< /highlight >}}

### **Linux：**
You can easily use Aspose.Diagram for Python via .NET from [pypi](https://pypi.org/project/aspose-diagram-python/)使用以下命令。
{{< highlight "NET" >}}

 $ pip install aspose-diagram-python

{{< /highlight >}}

## **Creating the Hello World Application**

- 创建一个名为**CreatingNewVisioFile.py**并使用以下示例代码：


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram()

#// Save diagram in the VSDX format
diagram.save("CreateNewVisio_out.vsdx", SaveFileFormat.VSDX)
{{< /highlight >}}


- 现在将上面的代码保存到“CreatingNewVisioFile.py”并运行“python CreatingNewVisioFile.py”@命令提示符。
