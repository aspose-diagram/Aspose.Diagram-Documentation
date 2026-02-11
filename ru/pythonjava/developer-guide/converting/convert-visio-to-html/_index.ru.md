---
title:  Преобразование Visio в формат HTML
linktitle: Преобразование Visio в HTML
type: docs
weight: 30
url: /ru/python-java/convert-visio-to-html/
description: This topic show you how to convert Visio to html formats using Aspose.Diagram for Python via Java. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM, VSSM to html with a few lines of code.
---
## **Экспорт Visio в HTML** ##
 В этой статье объясняется, как экспортировать Microsoft Visio diagram в HTML с помощью[Aspose.Diagram для Python via Java](https://products.aspose.com/diagram/python-java/) API.

Используйте конструктор класса Diagram для чтения файлов diagram и метод Save для экспорта diagram в любой поддерживаемый формат изображения. Разработчики могут сохранять результат HTML в локальном хранилище или непосредственно в экземпляре потока.

 На изображении ниже показан[VSD файл](ExportToHTML.vsd)будет сохранен в формате PNG. Вы можете использовать другие форматы diagram (VSDX, VSTM, VSTM, VSSX, VSS, VSSM, VDX, VST, VSTX, VDX, 04811103), а также 64 или 6411103.

**Введите diagram.**

![дело:изображение_альтернативный_текст](http://i.imgur.com/YX4BNNq.png)

Чтобы экспортировать VSD diagram в HTML, выполните следующие действия:

1. Создайте экземпляр класса Diagram.
1. Вызовите метод Save класса Dagram и установите HTML в качестве выходного формата.

На изображении ниже показан выходной файл HTML.

**Выход HTML diagram.**

![дело:изображение_альтернативный_текст](http://i.imgur.com/syavUqI.png)

### **Сохраните результат HTML в локальном хранилище.**
Полученный файл можно сохранить, передав полную строку пути, включая имя файла и расширение, например, @"c:\temp\MyOutput.html".

#### **Сохраните результат HTML в примере программирования локального хранилища**

{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# call the diagram constructor to load diagram from a VSD file
diagram = Diagram("ExportToHTML.vsd")

# Save as HTML
diagram.save("ExportToHTML_Out.html", SaveFileFormat.HTML)

jpype.shutdownJVM()

{{< /highlight >}}




### **Сохраните результат HTML в экземпляре потока.**
Это вариант использования для сохранения результирующего HTML в базе данных или репозитории без сохранения его в локальном хранилище. Эта функция также включает другие результирующие ресурсы HTML, например шрифты, CSS (содержащие информацию о стиле) и изображения. Поскольку он сохраняет один файл HTML в экземпляре потока.
#### **Сохраните результат HTML в образце потокового программирования**

{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load diagram
diagram = Diagram("ExportToHTML.vsd")
# save resultant HTML directly to a stream
dstStream = java.io.ByteArrayOutputStream()
diagram.save(dstStream, SaveFileFormat.HTML)
# In you want to read the result into a Diagram object again, you need to get the
# data bytes and wrap into an input stream.
# srcStream = java.io.ByteArrayInputStream(dstStream.toByteArray())

jpype.shutdownJVM()

{{< /highlight >}}

