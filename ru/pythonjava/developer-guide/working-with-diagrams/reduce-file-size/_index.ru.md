---
title: Уменьшить размер файла
type: docs
weight: 50
url: /ru/python-java/reduce-file-size/
description: В этом разделе объясняется, как уменьшить размер файла с diagram на Aspose.Diagram до Python via Java.
---
## **Уменьшить размер файла**
 Aspose.Diagram для Python via Java API позволяет разработчикам удалять скрытую информацию из diagram для уменьшения размера файла.
 Объект Page представляет область рисования страницы переднего плана или фоновой страницы. Чтобы уменьшить размер файла, вы можете использовать свойства RemoveHiddenInfoItem в**УдалитьСкрытуюИнформацию()** метод класса Diagram. В приведенном ниже примере кода показано, как удалить скрытую информацию из diagram.

```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Load a Visio diagram
diagram = Diagram("Drawing1.vsdx")

# Remove hidden information from diagram
diagram.removeHiddenInformation(RemoveHiddenInfoItem.SHAPES | RemoveHiddenInfoItem.MASTERS)

# save in the VSDX format
diagram.save("ReduceFileSize_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}
```
