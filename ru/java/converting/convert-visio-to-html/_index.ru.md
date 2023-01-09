---
title:  Преобразование Visio в формат HTML
linktitle: Преобразование Visio в HTML
type: docs
weight: 30
url: /ru/java/convert-visio-to-html/
description: В этом разделе показано, как Aspose.Diagram позволяет конвертировать Visio в форматы html. Преобразуйте VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM в html с помощью нескольких строк кода.
---
## **Экспорт Visio в HTML** **Экспорт Visio в HTML**
 В этой статье объясняется, как экспортировать Microsoft Visio diagram в HTML с помощью[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 Использовать[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) конструктор класса для чтения файлов diagram и метод Save для экспорта diagram в любой поддерживаемый формат изображения. Разработчики могут сохранять результат HTML в локальном хранилище или непосредственно в экземпляре потока.

1. [Сохраните результат HTML в локальном хранилище.](/diagram/ru/java/how-to-convert-a-visio-diagram/).
1. [Сохраните результат HTML в экземпляре потока.](/diagram/ru/java/how-to-convert-a-visio-diagram/).

На изображении ниже показан файл VSD, который нужно сохранить в формате PNG. Вы можете использовать другие форматы diagram (VSDX, VSTM, VSTM, VSSX, VSS, VSSM, VDX, VST, VSTX, VDX, 04811103 или .7

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
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToHTML-ExportToHTML.java" >}}



### **Сохраните результат HTML в экземпляре потока.**
Это вариант использования для сохранения результирующего HTML в базе данных или репозитории без сохранения его в локальном хранилище. Эта функция также включает другие результирующие ресурсы HTML, например шрифты, CSS (содержащие информацию о стиле) и изображения. Поскольку он сохраняет один файл HTML в экземпляре потока.
#### **Сохраните результат HTML в образце потокового программирования**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportHTMLinStream-ExportHTMLinStream.java" >}}
