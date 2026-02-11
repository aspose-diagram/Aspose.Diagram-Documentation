---
title: Отслеживание процесса преобразования документа
type: docs
weight: 970
url: /ru/java/track-document-conversion-progress/
description: В этом разделе объясняется, как отслеживать ход преобразования файлов visio с помощью Aspose.Diagram.
---
## **Возможные сценарии использования**

Иногда преобразование больших файлов visio может занять некоторое время. В это время вы можете захотеть показать ход преобразования документа, а не просто экран загрузки, чтобы повысить удобство использования вашего приложения. Aspose.Diagram поддерживает отслеживание процесса преобразования документов, предоставляя интерфейс IPageSavingCallback. Интерфейс IPageSavingCallback предоставляет методы PageStartSaving и PageEndSaving, которые можно реализовать в пользовательском классе. Вы также можете контролировать, какие страницы отображаются, как показано в T*estDiagramPageSavingCallback*пользовательский класс.

## **Отслеживание процесса преобразования документа**

 Следующий пример кода загружает[исходный файл visio](Drawing1.vsdx) и выводит ход преобразования в консоли с помощью команды*TestPageSavingCallback*пользовательский класс, реализующий интерфейс IPageSavingCallback.

## **Образец кода**


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(DetectFormatfromInputStream.class);

// Open the stream. Read only access to load a Visio diagram.
String stream = new String(dataDir + "Drawing1.vsdx");
// detect file format using an input stream
FileFormatInfo info = FileFormatUtil.detectFileFormat(stream);

// get the detected file format
System.out.println("The spreadsheet format is: " + info.getFileFormatType());

{{< /highlight >}}


Ниже приведен код для*Обратный вызов TestDiagramPageSaving*пользовательский класс.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(DetectFormatfromInputStream.class);

// Open the stream. Read only access to load a Visio diagram.
String stream = new String(dataDir + "Drawing1.vsdx");
// detect file format using an input stream
FileFormatInfo info = FileFormatUtil.detectFileFormat(stream);

// get the detected file format
System.out.println("The spreadsheet format is: " + info.getFileFormatType());

{{< /highlight >}}


## **Консольный вывод**

Начать сохранение индекса страницы 0 из страниц 11</br>
Завершить сохранение индекса страницы 0 из страниц 11</br>
Начать сохранение индекса страницы 1 из страниц 11</br>
Завершить сохранение индекса страницы 1 из страниц 11</br>
Начать сохранение указателя страниц 2 со страниц 11</br>
Завершить сохранение указателя страниц 2 из страниц 11</br>
Начать сохранение указателя страницы 3 из страниц 11</br>
Завершить сохранение указателя страниц 3 из страниц 11</br>
Начать сохранение указателя страниц 4 из страниц 11</br>
Завершить сохранение указателя страниц 4 из страниц 11</br>
Начать сохранение индекса страницы 5 из страниц 11</br>
Завершить сохранение индекса страницы 5 из страниц 11</br>
Начать сохранение указателя страницы 6 из страниц 11</br>
Завершить сохранение указателя 6 страницы из 11</br>
Начать сохранение индекса страницы 7 из страниц 11</br>
Завершить сохранение оглавления страницы 7 из страниц 11</br>
Начать сохранение указателя страницы 8 из страниц 11</br>
Завершить сохранение индекса страницы 8 из страниц 11
