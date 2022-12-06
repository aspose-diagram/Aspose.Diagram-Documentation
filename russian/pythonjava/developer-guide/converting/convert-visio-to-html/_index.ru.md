---
title:  Преобразование Visio в формат HTML
linktitle: Конвертировать Visio в HTML
type: docs
weight: 30
url: /ru/python-java/convert-visio-to-html/
description: This topic show you how to convert Visio to html formats using Aspose.Diagram for Python via Java. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM, VSSM to html with a few lines of code.
---
## **Экспорт Visio в HTML** ##
 В этой статье объясняется, как экспортировать Microsoft Visio diagram в HTML с помощью[Aspose.Diagram для Python через Java](https://products.aspose.com/diagram/python-java/) API.

Используйте конструктор класса Diagram для чтения файлов diagram и метод Save для экспорта diagram в любой поддерживаемый формат изображения. Разработчики могут сохранять полученный HTML-код в локальном хранилище или непосредственно в экземпляре потока.

 На изображении ниже показан[VSD файл](ExportToHTML.vsd)будет сохранен в формате PNG. Вы также можете использовать другие форматы diagram (VSDX, VSTM, VSTM, VSSX, VSS, VSSM, VDX, VST, VSTX, VDX, VTX или 048111).

**Введите diagram.**

![дело:изображение_альтернативный_текст](http://i.imgur.com/YX4BNNq.png)

Чтобы экспортировать VSD diagram в HTML, выполните следующие действия:

1. Создайте экземпляр класса Diagram.
1. Вызовите метод Save класса Dagram и установите HTML в качестве выходного формата.

На изображении ниже показан выходной HTML-файл.

**Выведите HTML diagram.**

![дело:изображение_альтернативный_текст](http://i.imgur.com/syavUqI.png)

### **Сохраните полученный HTML в локальном хранилище**
Полученный файл можно сохранить, передав полную строку пути, включая имя файла и расширение, например, @"c:\temp\MyOutput.html".

#### **Сохранение результирующего HTML в примере программирования локального хранилища**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToHTML.py" >}}



### **Сохраните полученный HTML в экземпляре потока**
Это вариант использования для сохранения результирующего HTML в базе данных или репозитории без сохранения его в локальном хранилище. Эта функция также включает другие результирующие ресурсы HTML, например, шрифты, CSS (содержащие информацию о стиле) и изображения. Поскольку он сохраняет один файл HTML в экземпляре потока.
#### **Сохранение результирующего HTML в примере потокового программирования**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportHTMLinStream.py" >}}
