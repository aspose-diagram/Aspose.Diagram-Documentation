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

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-DiagramConversions-GetWarningInformation.cs" >}}

## **Консольный вывод**

Вот консольный вывод приведенного выше кода при выполнении с предоставленным[образец файла visio](sampleFontSubstitution.vsdx).

{{< highlight "java" >}}
Font substitution: Font [ Athene Logos ]has been substituted by Font[Times New Roman]{{< /highlight >}}
