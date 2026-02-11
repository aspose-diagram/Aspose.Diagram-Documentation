---
title: Начиная
linktitle: Начиная
type: docs
weight: 4
url: /ru/python-net/getting-started/ 
keywords: python, visio, instal
description: Настройка Aspose.Diagram для Python via .NET и инструкции по установке.
---
## **Системные Требования**
 Aspose.Diagram для Python via .NET не зависит от платформы API и может использоваться на любой платформе (Windows и Linux), где[Python](https://www.python.org/downloads/) установлен.

## **Python Версия**
- Python 3.6 или выше

## **Монтаж**
### **Windows:**
 Вы можете легко использовать Aspose.Diagram для Python via .NET из[pypi](https://pypi.org/project/aspose-diagram-python/) с помощью следующей команды.
{{< highlight "NET" >}}

 $ pip install aspose-diagram-python

{{< /highlight >}}

### **Линукс:**
 Вы можете легко использовать Aspose.Diagram для Python via .NET из[pypi](https://pypi.org/project/aspose-diagram-python/) с помощью следующей команды.
{{< highlight "NET" >}}

 $ pip install aspose-diagram-python

{{< /highlight >}}

## **Создание приложения Hello World**

-  Создайте файл с именем**СозданиеNewVisioFile.py** и используйте следующий пример кода:


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram()

#// Save diagram in the VSDX format
diagram.save("CreateNewVisio_out.vsdx", SaveFileFormat.VSDX)
{{< /highlight >}}


- Теперь сохраните приведенный выше код в «CreatingNewVisioFile.py» и запустите командную строку «python MakingNewVisioFile.py».
