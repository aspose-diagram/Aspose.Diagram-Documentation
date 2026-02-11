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

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// create an instance PDF save options class
Aspose.Diagram.Saving.PdfSaveOptions options = new Aspose.Diagram.Saving.PdfSaveOptions();
          
//set page saving call back
options.PageSavingCallback = new TestDiagramPageSavingCallback();

// save Visio drawing
diagram.Save(dataDir + "Callback_out.pdf", options);

{{< /highlight >}}
```

Ниже приведен код для*Обратный вызов TestDiagramPageSaving*пользовательский класс.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
public class TestDiagramPageSavingCallback : Aspose.Diagram.Saving.IPageSavingCallback
{
    public void PageStartSaving(Aspose.Diagram.Saving.PageStartSavingArgs args)
    {
        Console.WriteLine("Start saving diagram page index {0} of pages {1}", args.PageIndex, args.PageCount);
    }

    public void PageEndSaving(Aspose.Diagram.Saving.PageEndSavingArgs args)
    {
        Console.WriteLine("End saving diagram page index {0} of pages {1}", args.PageIndex, args.PageCount);

        //don't output pages after page index 8.
        if (args.PageIndex >= 8)
        {
            args.HasMorePages = false;
        }
    }
}

{{< /highlight >}}
```

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
