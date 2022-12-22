---
title: Отслеживание процесса преобразования документа
type: docs
weight: 970
url: /ru/net/track-document-conversion-progress/
description: В этом разделе объясняется, как отслеживать ход преобразования файлов visio с помощью Aspose.Diagram.
---
## **Возможные сценарии использования**

 Иногда преобразование больших файлов visio может занять некоторое время. В это время вы можете захотеть показать ход преобразования документа, а не просто экран загрузки, чтобы повысить удобство использования вашего приложения. Aspose.Diagram поддерживает процесс преобразования документа отслеживания, предоставляя**[IPageSavingCallback] (https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback)** интерфейс.**[IPageSavingCallback] (https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback)**интерфейс обеспечивает**[PageStartSaving](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback/methods/pagestartsaving)**а также**[PageEndSaving](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback/methods/pageendsaving)**методы, которые вы можете реализовать в своем пользовательском классе. Вы также можете контролировать, какие страницы отображаются, как показано в T*estDiagramPageSavingCallback*пользовательский класс.

## **Отслеживание процесса преобразования документа**

 Следующий пример кода загружает[исходный файл visio](Drawing1.vsdx) и выводит ход преобразования в консоли с помощью команды*TestPageSavingCallback* пользовательский класс, который реализует**[IPageSavingCallback] (https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback)**интерфейс.

## **Образец кода**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-DiagramConversions-DocumentConversionProgress-1.cs" >}}

Ниже приведен код для*Обратный вызов TestDiagramPageSaving*пользовательский класс.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-DiagramConversions-DocumentConversionProgress-2.cs" >}}

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
