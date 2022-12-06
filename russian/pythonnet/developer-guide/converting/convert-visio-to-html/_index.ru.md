---
title:  Преобразование Visio в формат HTML
linktitle: Конвертировать Visio в HTML
type: docs
weight: 30
url: /ru/python-net/convert-visio-to-html/
description: В этом разделе показано, как Aspose.Diagram позволяет конвертировать Visio в форматы html. Преобразуйте VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM в html с помощью нескольких строк кода.
---
## **Экспорт Visio в HTML**
 В этой статье объясняется, как экспортировать Microsoft Visio diagram в HTML с помощью[Aspose.Diagram для Python через .NET](https://products.aspose.com/diagram/python-net/) API.

Используйте конструктор класса Diagram для чтения файлов diagram и метод Save для экспорта diagram в любой поддерживаемый формат изображения. Разработчики могут сохранять полученный HTML-код в локальном хранилище или непосредственно в экземпляре потока.

1. [Сохраните полученный HTML в локальном хранилище](https://docs.aspose.com/diagram/net/convert-visio-to-html/#save-resultant-html-in-the-local-storage).
1. [Сохраните полученный HTML в экземпляре потока](https://docs.aspose.com/diagram/net/convert-visio-to-html/#save-resultant-html-in-a-stream-instance).

На изображении ниже показан файл VSD, который нужно сохранить в формате PNG. Вы также можете использовать другие форматы diagram (VSDX, VSDM, VSTX, VSSX, VSS, VSSM, VDX, VST, VSTX, VDX, VTX или 1 076181).

|**Введите diagram.**|
|:- |
|![дело:изображение_альтернативный_текст](how-to-convert-a-visio-diagram_6.png)|
Чтобы экспортировать VSD diagram в HTML, выполните следующие действия:

1. Создайте экземпляр класса Diagram.
1. Вызовите метод Save класса Dagram и установите HTML в качестве выходного формата.
### **Сохраните полученный HTML в локальном хранилище**
Полученный файл можно сохранить, передав полную строку пути, включая имя файла и расширение, например, @"c:\temp\MyOutput.html".
#### **Сохранение результирующего HTML в примере программирования локального хранилища**
{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-ExportToHTML.py" >}}
