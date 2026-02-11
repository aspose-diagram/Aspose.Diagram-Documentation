---
title: Başlarken
linktitle: Başlarken
type: docs
weight: 4
url: /tr/python-net/getting-started/ 
keywords: python, visio, instal
description: Python via .NET için kurulum Aspose.Diagram ve kurulum yönergeleri.
---
## **sistem gereksinimleri**
 Python via .NET için Aspose.Diagram, platformdan bağımsızdır API ve herhangi bir platformda (Windows ve Linux) kullanılabilir.[Python](https://www.python.org/downloads/) kurulur.

## **Python Versiyon**
- Python 3.6 veya üstü

## **Kurulum**
### **Windows:**
 Python via .NET için Aspose.Diagram den rahatlıkla kullanabilirsiniz.[pypi](https://pypi.org/project/aspose-diagram-python/) aşağıdaki komutla.
{{< highlight "NET" >}}

 $ pip install aspose-diagram-python

{{< /highlight >}}

### **Linux:**
 Python via .NET için Aspose.Diagram den rahatlıkla kullanabilirsiniz.[pypi](https://pypi.org/project/aspose-diagram-python/) aşağıdaki komutla.
{{< highlight "NET" >}}

 $ pip install aspose-diagram-python

{{< /highlight >}}

## **Hello World Uygulamasını Oluşturma**

-  adlı bir dosya oluşturun.**OluşturmaNewVisioFile.py** ve aşağıdaki örnek kodu kullanın:


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram()

#// Save diagram in the VSDX format
diagram.save("CreateNewVisio_out.vsdx", SaveFileFormat.VSDX)
{{< /highlight >}}


- Şimdi yukarıdaki kodu "CreatingNewVisioFile.py"ye kaydedin ve "python CreateNewVisioFile.py" @command istemini çalıştırın.
