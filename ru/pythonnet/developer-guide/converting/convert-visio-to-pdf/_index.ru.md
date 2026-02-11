---
title:  Преобразование Visio в формат PDF
linktitle: Преобразование Visio в PDF
type: docs
weight: 10
url: /ru/python-net/convert-visio-to-pdf/
description: В этом разделе показано, как Aspose.Diagram позволяет конвертировать форматы Visio в PDF. Преобразуйте VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM в PDF с помощью нескольких строк кода.
---
## **Экспорт в PDF**
{{% alert color="primary" %}}

 Aspose.Diagram для Python via .NET непосредственно записывает информацию о API и номере версии в выходных документах. Например, при отображении чертежа на PDF, Aspose.Diagram for .NET заполняет**Заявление** поле со значением «Aspose.Diagram» и**PDF Продюсер** поле со значением, например 'Aspose.Diagram 17.9'.

Обратите внимание, что вы не можете поручить Aspose.Diagram for .NET API изменить или удалить эту информацию из выходных документов.

{{% /alert %}}

 В этой статье объясняется, как экспортировать Microsoft Visio diagram в PDF с помощью[Aspose.Diagram для Python via .NET](https://products.aspose.com/diagram/python-net/) API.

Используйте конструктор класса [Diagram] для чтения файлов diagram и метод Save для экспорта diagram в любой поддерживаемый формат изображения.

На изображении ниже показан VSD diagram, который фрагменты кода ниже экспортируют PDF. Вы можете использовать другие форматы diagram (VSS, VSSM, VDX, VST, VSTX, VDX, 08161081, 08161081 или 34.64 или 34.

|**Исходный файл.**|
|:- |
|![дело:изображение_альтернативный_текст](how-to-convert-a-visio-diagram_1.png)|


Чтобы экспортировать VSD diagram в PDF:

1. Создайте экземпляр класса Diagram.
1. Вызовите метод Save классов Diagram и установите выходной формат PDF.

Ниже приведено изображение выходного файла PDF.

|**Выходной файл PDF.**|
|:- |
|![дело:изображение_альтернативный_текст](how-to-convert-a-visio-diagram_2.png)|
### **Экспорт Microsoft Visio Чертеж в PDF**
В примерах кода показано, как экспортировать чертеж Microsoft Visio в PDF с помощью Python.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the pdf format
diagram.save("Visio_out.pdf", SaveFileFormat.PDF)
{{< /highlight >}}

