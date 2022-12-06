---
title:  Преобразование Visio в формат HTML
linktitle: Преобразование Visio в HTML
type: docs
weight: 30
url: /ru/net/convert-visio-to-html/
description: В этом разделе показано, как Aspose.Diagram позволяет конвертировать Visio в форматы html. Преобразуйте VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM в html с помощью нескольких строк кода.
---
## **Экспорт Visio в HTML**
 В этой статье объясняется, как экспортировать Microsoft Visio diagram в HTML с помощью[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API.

 Использовать[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) конструктор класса для чтения файлов diagram и метод Save для экспорта diagram в любой поддерживаемый формат изображения. Разработчики могут сохранять результат HTML в локальном хранилище или непосредственно в экземпляре потока.

1. [Сохраните результат HTML в локальном хранилище.](https://docs.aspose.com/diagram/net/convert-visio-to-html/#save-resultant-html-in-the-local-storage).
1. [Сохраните результат HTML в экземпляре потока.](https://docs.aspose.com/diagram/net/convert-visio-to-html/#save-resultant-html-in-a-stream-instance).

На изображении ниже показан файл VSD, который нужно сохранить в формате PNG. Вы можете использовать другие форматы diagram (VSDX, VSDM, VSTX, VSSX, VSS, VSSM, VDX, VST, VSTX, VDX, 04811103 или .7

|**Введите diagram.**|
|:- |
|![дело:изображение_альтернативный_текст](how-to-convert-a-visio-diagram_6.png)|
Чтобы экспортировать VSD diagram в HTML, выполните следующие действия:

1. Создайте экземпляр класса Diagram.
1. Вызовите метод Save класса Dagram и установите HTML в качестве выходного формата.
### **Сохраните результат HTML в локальном хранилище.**
Полученный файл можно сохранить, передав полную строку пути, включая имя файла и расширение, например, @"c:\temp\MyOutput.html".
#### **Сохраните результат HTML в примере программирования локального хранилища**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-ExportToHTML-ExportToHTML.cs" >}}



### **Сохраните результат HTML в экземпляре потока.**
Это вариант использования для сохранения результирующего HTML в базе данных или репозитории без сохранения его в локальном хранилище. Эта функция также включает другие результирующие ресурсы HTML, например шрифты, CSS (содержащие информацию о стиле) и изображения. Поскольку он сохраняет один файл HTML в экземпляре потока.
#### **Сохраните результат HTML в образце потокового программирования**
{{< highlight "java" >}}

 // Load an existing visio diagram

Diagram diagram = new Diagram("Basic Flowchart.vsd");

// Save resultant HTML directly to a stream

MemoryStream stream = new MemoryStream();

diagram.Save(stream, SaveFileFormat.HTML);



{{< /highlight >}}
