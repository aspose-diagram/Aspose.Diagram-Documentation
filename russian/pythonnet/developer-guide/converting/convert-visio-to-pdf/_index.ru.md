---
title:  Конвертировать Visio в формат PDF
linktitle: Конвертировать Visio в PDF
type: docs
weight: 10
url: /ru/python-net/convert-visio-to-pdf/
description: В этом разделе показано, как Aspose.Diagram позволяет конвертировать Visio в форматы PDF. Конвертируйте VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM в PDF с помощью нескольких строк кода.
---
## **Экспорт в PDF**
{{% alert color="primary" %}}

Aspose.Diagram для Python через .NET непосредственно записывает информацию о API и номере версии в выходных документах. Например, при рендеринге чертежа в PDF Aspose.Diagram for .NET заполняется**Заявление** поле со значением «Aspose.Diagram» и**PDF-продюсер** поле со значением, например 'Aspose.Diagram 17.9'.

Обратите внимание, что вы не можете поручить Aspose.Diagram for .NET API изменить или удалить эту информацию из выходных документов.

{{% /alert %}}

 В этой статье объясняется, как экспортировать Microsoft Visio diagram в PDF, используя[Aspose.Diagram для Python через .NET](https://products.aspose.com/diagram/python-net/) API.

Используйте конструктор класса [Diagram] для чтения файлов diagram и метод Save для экспорта diagram в любой поддерживаемый формат изображения.

На изображении ниже показан код VSD diagram, который фрагменты кода ниже экспортируют в PDF. Вы также можете использовать другие форматы diagram (VSS, VSSM, VDX, VST, VSTX, VDX, VTX или VSX).

|**Исходный файл.**|
|:- |
|![дело:изображение_альтернативный_текст](how-to-convert-a-visio-diagram_1.png)|


Чтобы экспортировать VSD diagram в PDF:

1. Создайте экземпляр класса Diagram.
1. Вызовите метод сохранения классов Diagram и установите выходной формат PDF.

Ниже приведено изображение выходного PDF-файла.

|**Выходной PDF-файл.**|
|:- |
|![дело:изображение_альтернативный_текст](how-to-convert-a-visio-diagram_2.png)|
### **Экспорт Microsoft Visio Чертеж в PDF**
В примерах кода показано, как экспортировать чертеж Microsoft Visio в PDF с помощью Python.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-ExportToPdf.py" >}}
