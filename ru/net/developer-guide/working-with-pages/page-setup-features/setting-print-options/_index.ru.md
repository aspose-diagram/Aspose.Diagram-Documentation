---
title: Настройка параметров печати
type: docs
weight: 10
url: /ru/net/setting-print-options/
description: В этом разделе объясняется, как установить параметры печати с помощью Aspose.Diagram.
---
{{% alert color="primary" %}}

Иногда необходимо настроить параметры страницы для управления печатью. Эти параметры настройки страницы предлагают различные варианты.

{{% /alert %}}

## **Настройка параметров печати**

Параметры настройки страницы полностью поддерживаются в Aspose.Diagram. В этой статье объясняется, как установить параметры страницы с помощью Aspose.Diagram, и показаны примеры кода для настройки:

 Aspose.Diagram предоставляет класс,[**Страница**](https://reference.aspose.com/diagram/net/aspose.diagram/page) , представляющий файл Microsoft Visio.[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/page) класс содержит[**Страницы**](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection) коллекция, которая позволяет получить доступ к каждой странице в файле Visio. Страница представлена[**Страница**](https://reference.aspose.com/diagram/net/aspose.diagram/page)учебный класс.

[**СтраницаЛист**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) класс обеспечивает[**PrintProps**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) свойство, которое используется для установки параметров настройки страницы. На самом деле это[**PrintProps**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) имущество – это объект[**СтраницаЛист**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) класс, используемый для установки различных параметров макета страницы для печатной страницы.[**PrintProps**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops)Класс предоставляет различные свойства, используемые для установки параметров настройки страницы. Некоторые из этих свойств обсуждаются ниже.

### **Ориентация страницы печати**

 Ориентация страницы печати может быть установлена на книжную или альбомную с помощью[**PrintProps**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) учебный класс'[**PrintPageOrientation**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/printpageorientation) имущество.[**PrintPageOrientation**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/printpageorientation) свойство принимает одно из предопределенных значений в[**Принтпажеориентатионвалуе**](https://reference.aspose.com/diagram/net/aspose.diagram/printpageorientationvalue)перечисление, приведенное ниже.

|**Типы ориентации страницы печати**|**Описание**|
|:- |:- |
|Самеаспринтер|То же, что и ориентация принтера|
|Пейзаж|Альбомная ориентация|
|Портрет|Портретная ориентация|


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Print();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

//Get page
Aspose.Diagram.Page page = diagram.Pages.GetPage(0);

//Set PrintPageOrientation
page.PageSheet.PrintProps.PrintPageOrientation.Value = PrintPageOrientationValue.Landscape;

{{< /highlight >}}


### **Коэффициент масштабирования**

 Можно уменьшить или увеличить размер страницы, отрегулировав коэффициент масштабирования с помощью[**МасштабX**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/scalex)имущество.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Print();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

//Set ScaleX and ScaleY
diagram.Pages[0].PageSheet.PrintProps.ScaleX.Value = 1;
diagram.Pages[0].PageSheet.PrintProps.ScaleY.Value = 1;

{{< /highlight >}}

