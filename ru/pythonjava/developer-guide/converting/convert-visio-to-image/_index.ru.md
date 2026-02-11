---
title:  Конвертировать Visio в форматы изображений
linktitle: Преобразовать Visio в изображения
type: docs
weight: 20
url: /ru/python-java/convert-visio-to-image/
description: This topic show you how to convert Visio to various images formats using Aspose.Diagram for Python via Java. Convert Visio,VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM, VSSM to PNG, JPEG, BMP images with a несколько строк кода.
---
## **Экспорт диаграмм в форматы файлов изображений**
В этой статье объясняется, как экспортировать Microsoft Visio diagram в изображение, используя Aspose.Diagram для Python via Java.

Используйте конструктор класса Diagram для чтения файлов diagram и метод Save для экспорта diagram в любой поддерживаемый формат изображения. На изображении ниже показан файл VSD, который будет сохранен в формате PNG. Вы также можете использовать другие форматы diagram (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX или VSX).

**[Пример файла VSD.](ExportToImage.vsd)**

Чтобы экспортировать diagram в изображение:

- Создайте экземпляр класса Diagram.
- Вызовите метод Save класса Diagram и установите формат изображения, в который вы хотите экспортировать. Выходной файл изображения выглядит как исходный файл.

**Выходной файл PNG.**

![дело:изображение_альтернативный_текст](ExportToImage.png)
### **Пример программирования экспорта в файл изображения**
```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Call the diagram constructor to load diagram from a VSD file
diagram = Diagram("ExportToImage.vsd")

# Save as PNG
diagram.save("ExportToImage_Out.png", SaveFileFormat.PNG)

jpype.shutdownJVM()

{{< /highlight >}}
```

Также можно сохранить в изображение определенную страницу, а не весь документ:

```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load diagram
diagram = Diagram("ExportToImage.vsd")

# Save diagram as PNG
options = ImageSaveOptions(SaveFileFormat.PNG)

# Save one page only, by page index
options.setPageIndex(0)

# Save resultant Image file
diagram.save("ExportPageToImage_Out.png", options)

jpype.shutdownJVM()

{{< /highlight >}}
```