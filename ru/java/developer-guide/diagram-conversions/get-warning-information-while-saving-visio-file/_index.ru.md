---
title: Получить предупреждающую информацию при сохранении файла Visio
type: docs
weight: 110
url: /ru/java/get-warning-information-while-saving-visio-file/
---
## **Возможные сценарии использования**

 Иногда пользователь пытается сохранить diagram, который содержит текст, не имеющий локального шрифта. В таком случае Aspose.Diagram выдает предупреждения при сохранении diagram. Вы можете поймать эти предупреждения, внедрив**[IWarningCallback](https://reference.aspose.com/diagram/net/aspose.diagram/iwarningcallback)** интерфейс и настройка**[SaveOptions.WarningCallback](https://reference.aspose.com/diagram/net/aspose.diagram.saving/saveoptions/properties/warningcallback)**имущество.

## **Получать предупреждения при сохранении файла Visio**

 В следующем примере кода объясняется, как получать предупреждения при сохранении файла visio. Код преобразует[образец файла visio](sampleFontSubstitution.vsdx) который бросает**[Подстановка шрифта] (https://reference.aspose.com/diagram/net/aspose.diagram/warningtype)** предупреждение о сохранении. Затем это предупреждение перехватывается**[IWarningCallback.Warning()](https://reference.aspose.com/diagram/net/aspose.diagram/iwarningcallback/methods/warning)**метод, выводящий предупреждающие сообщения на консоль. Пожалуйста, также проверьте консольный вывод кода, приведенного ниже, для большего понимания.

## **Образец кода**

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// call the diagram constructor to load diagram from a VSDX file
Diagram diagram = new Diagram(dataDir + "sampleFontSubstitution.vsdx");

// create an instance SVG save options class
Aspose.Diagram.Saving.SVGSaveOptions so = new Aspose.Diagram.Saving.SVGSaveOptions();

so.WarningCallback = new TestDiagramWarningCallback();
// save Visio drawing
diagram.Save(dataDir + "WarningCallback_out.svg", options);


public class TestDiagramWarningCallback : Aspose.Diagram.IWarningCallback
{
    public void Warning(Aspose.Diagram.WarningInfo info)
    {
        if (info.WarningType == Aspose.Diagram.WarningType.FontSubstitution)
        {
            Console.WriteLine("Diagram WARNING INFO: " + info.Description);
        }

    }
}

{{< /highlight >}}
```

## **Консольный вывод**

Вот консольный вывод приведенного выше кода при выполнении с предоставленным[образец файла visio](sampleFontSubstitution.vsdx).

{{< highlight "java" >}}
Font substitution: Font [ Athene Logos ]has been substituted by Font[Times New Roman]{{< /highlight >}}
