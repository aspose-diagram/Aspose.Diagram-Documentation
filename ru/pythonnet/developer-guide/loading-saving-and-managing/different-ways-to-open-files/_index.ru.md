---
title: Различные способы открытия файлов
type: docs
weight: 10
url: /ru/python-net/different-ways-to-open-files/
---
{{% alert color="primary" %}}

С Aspose.Diagram легко открывать файлы, например, для получения данных или использовать шаблон конструктора для ускорения процесса разработки.

{{% /alert %}}

## **Открытие файла via Путь**

 Разработчики могут открыть файл Microsoft Diagram, используя его путь к файлу на локальном компьютере, указав его в**Diagram**конструктор класса. Просто передайте путь в конструкторе как*нить*. Aspose.Diagram автоматически определит тип формата файла.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the VSDX format
diagram.save("CreateNewVisio_out.vsdx", SaveFileFormat.VSDX)
{{< /highlight >}}


## **Открытие файла via в потоке**

 Также просто открыть файл Visio в виде потока. Для этого используйте перегруженную версию конструктора, который принимает*BufferStream*объект, содержащий файл.


{{< highlight python >}}
import os
import sys
import aspose.diagram
from aspose.diagram import *
from aspose.pyio import BufferStream

#// Build path of an existing diagram
visioDrawing = os.path.join(sourceDir, "Drawing1.vsdx")
# Create a Stream object
f = open(visioDrawing, 'rb')
data = f.read()
databuff = BufferStream(data)
diagram = Diagram(databuff)

#// Save diagram in the VSDX format
diagram.save("Visio_out.vsdx", SaveFileFormat.VSDX)
{{< /highlight >}}


## **Открытие файла с помощью LoadOptions**

 Чтобы открыть файл с параметрами загрузки, используйте команду**Параметры загрузки**классы, чтобы установить соответствующие параметры классов для загружаемого файла шаблона.


{{< highlight python >}}
import os
import sys
import aspose.diagram
from aspose.diagram import *

#// Build path of an existing diagram
visioDrawing = os.path.join(sourceDir, "Drawing1.vsdx")
# Instantiate LoadOptions specified by the LoadFileFormat
loadOptions = LoadOptions(LoadFileFormat.VSDX)
diagram = Diagram(visioDrawing,loadOptions)

#// Save diagram in the VSDX format
diagram.save("Visio_out.vsdx", SaveFileFormat.VSDX)
{{< /highlight >}}


