---
title: Слияние Комбинат Diagram
type: docs
weight: 30
url: /ru/python-java/merge-combine-diagram/
description: В этом разделе объясняется, как объединить файл visio
---
## **Возможные сценарии использования**

Aspose.Diagram для Python via Java позволяет объединить два файла visio в один.
Aspose.Diagram для Python via Java API имеет класс Diagram, который представляет чертеж Visio.
Использование метода**Объединить** в классе Diagram для объединения диаграмм.

## **Образец кода**

{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Load a Visio diagram
diagram = Diagram("Drawing1.vsdx")

# Load another Visio diagram
diagram2 = Diagram("DrawingFlowChart.vsdx")

diagram2.combine(diagram)

# save in the VSDX format
diagram2.save("CombineDiagram_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

