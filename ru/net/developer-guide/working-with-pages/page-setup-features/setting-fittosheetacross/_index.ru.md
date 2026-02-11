---
title: Настройка FitToSheetAcross
type: docs
weight: 10
url: /ru/net/setting-fittosheetacross/
description: В этом разделе объясняется, как настроить fittosheet с помощью Aspose.Diagram.
---
{{% alert color="primary" %}}

Иногда необходимо настроить параметры страницы для управления печатью. Эти параметры настройки страницы предлагают различные варианты.

{{% /alert %}}

## **Настройка FitToSheetAcross**

Параметры настройки страницы полностью поддерживаются в Aspose.Diagram. В этой статье объясняется, как установить параметры страницы с помощью Aspose.Diagram, и показаны примеры кода для настройки:

 Aspose.Diagram предоставляет класс,[**Страница**](https://reference.aspose.com/diagram/net/aspose.diagram/page) , представляющий файл Microsoft Visio.[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/page) класс содержит[**Страницы**](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection) коллекция, которая позволяет получить доступ к каждой странице в файле Visio. Страница представлена[**Страница**](https://reference.aspose.com/diagram/net/aspose.diagram/page)учебный класс.

[**СтраницаЛист**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) класс обеспечивает[**PrintProps**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) свойство, которое используется для установки параметров настройки страницы. На самом деле это[**PrintProps**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) имущество – это объект[**СтраницаЛист**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) класс, используемый для установки различных параметров макета страницы для печатной страницы.[**PrintProps**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops)Класс предоставляет различные свойства, используемые для установки параметров настройки страницы. Некоторые из этих свойств обсуждаются ниже.

### **FitToSheetAcross**

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Print();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

PrintProps printProps = diagram.Pages[0].PageSheet.PrintProps;

printProps.OnPage.Value = BOOL.True;

//Set Fit to sheet(s) across
printProps.PagesX.Value = 1;

//Set By sheet(s) down
printProps.PagesY.Value = 1;

{{< /highlight >}}
```


