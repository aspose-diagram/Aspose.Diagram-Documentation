---
title:  Преобразование Visio в формат PDF
linktitle: Преобразование Visio в PDF
type: docs
weight: 10
url: /ru/python-java/convert-visio-to-pdf/
description: This topic show you how to convert Visio to PDF formats using Aspose.Diagram for Python via Java. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM, VSSM to PDF with a few lines of code.
---
## **Экспорт на PDF**
{{% alert color="primary" %}}

Aspose.Diagram для Python via Java непосредственно записывает информацию о API и номере версии в выходных документах. Например, при отображении чертежа на PDF, Aspose.Diagram for Java заполняет**Заявление**поле со значением «Aspose.Diagram» и**PDF Продюсер**поле со значением, например «Aspose.Diagram 17,9».

Обратите внимание, что вы не можете поручить Aspose.Diagram для Python via Java изменить или удалить эту информацию из выходных документов.

{{% /alert %}}

В этой статье объясняется, как экспортировать Microsoft Visio diagram в PDF, используя Aspose.Diagram для Python via Java.

Используйте конструктор класса Diagram для чтения файлов diagram и метод Save для экспорта diagram в любой поддерживаемый формат изображения.

[VSD diagram](ExportToPDF.vsd)является примером файла чертежа для экспорта PDF. Вы можете использовать другие форматы diagram (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX) или 3.47810, а также

Чтобы экспортировать VSD diagram в PDF:

1. Создайте экземпляр класса Diagram.
1. Вызовите метод Save классов Diagram и установите выходной формат PDF.

### **Экспорт в PDF Образец программы**
```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Call the diagram constructor to load diagram from a VSD file
diagram = Diagram("ExportToPDF.vsd")

# Save as PDF file format
diagram.save("ExportToPDF_Out.pdf", SaveFileFormat.PDF)

jpype.shutdownJVM()

{{< /highlight >}}
```

### **Разделить несколько страниц**
Aspose.Diagram for Java позволяет разделить несколько страниц при преобразовании Microsoft Visio Diagram в PDF. В следующем фрагменте кода показана функциональность.

```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Call the diagram constructor to load diagram from a VSDX file
diagram = Diagram("Network Diagram_start.vsdx")
# Options when saving a diagram into the PDF format
options = PdfSaveOptions()
# set SplitMultiPages option
options.setSplitMultiPages(True)
# save in PDF format
diagram.save("SplitMultiPages.pdf", options)

jpype.shutdownJVM()

{{< /highlight >}}
```
