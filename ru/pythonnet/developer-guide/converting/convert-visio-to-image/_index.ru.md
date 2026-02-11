---
title:  Конвертировать Visio в форматы изображений
linktitle: Преобразовать Visio в изображения
type: docs
weight: 20
url: /ru/python-net/convert-visio-to-image/
description: В этом разделе показано, как Aspose.Diagram позволяет конвертировать Visio в различные форматы изображений. Конвертируйте Visio,VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM в изображения PNG, JPEG, BMP с помощью нескольких строк кода.
---
## **Экспорт диаграмм в форматы файлов изображений**
 В этой статье объясняется, как экспортировать Microsoft Visio diagram в изображение с помощью[Aspose.Diagram for .NET](https://products.aspose.com/diagram/python-net/) API. Используйте конструктор класса [Diagram] для чтения файлов diagram и метод Save для экспорта diagram в любой поддерживаемый формат изображения.

Чтобы экспортировать diagram в изображение:

- Создайте экземпляр класса Diagram.
- Вызовите метод Save класса Diagram и установите формат изображения, в который вы хотите экспортировать. Выходной файл изображения выглядит как исходный файл.
### **Экспорт Microsoft Visio чертежа в файл изображения**

{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the png format
diagram.save("Visio_out.png", SaveFileFormat.PNG)
{{< /highlight >}}


Также можно сохранить в изображение определенную страницу, а не весь документ:


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))
#// Save diagram as PNG
options = saving.ImageSaveOptions(SaveFileFormat.PNG)
    
#// Save one page only, by page index
options.page_index = 0

#// Save diagram in the png format
diagram.save("ExportPageToImage_out.png", options)
{{< /highlight >}}
