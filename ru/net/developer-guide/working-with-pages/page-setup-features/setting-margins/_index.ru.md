---
title: Настройка полей
type: docs
weight: 20
url: /ru/net/setting-margins/
description: В этом разделе объясняется, как установить параметры страницы visio с помощью Aspose.Diagram.
---
{{% alert color="primary" %}}

Aspose.Diagram полностью поддерживает параметры настройки страницы Microsoft Visio. Разработчикам может потребоваться настроить параметры страницы для управления процессом печати. В этом разделе обсуждается, как использовать Aspose.Diagram для настройки полей страницы.

{{% /alert %}}

## **Настройка полей**

 Aspose.Diagram предоставляет класс,[**Страница**](https://reference.aspose.com/diagram/net/aspose.diagram/page) , представляющий файл Microsoft Visio.[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/page) класс содержит[**Страницы**](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection) коллекция, которая позволяет получить доступ к каждой странице в файле Visio. Страница представлена[**Страница**](https://reference.aspose.com/diagram/net/aspose.diagram/page)учебный класс.

[**СтраницаЛист**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) класс обеспечивает[**PrintProps**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) свойство, которое используется для установки параметров настройки страницы. На самом деле это[**PrintProps**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) имущество – это объект[**СтраницаЛист**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) класс, используемый для установки различных параметров макета страницы для печатной страницы.[**PrintProps**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops)Класс предоставляет различные свойства, используемые для установки параметров настройки страницы. Некоторые из этих свойств обсуждаются ниже.

### **Поля страницы**

 Установите поля страницы (PageTopMargin, PageBottomMargin, PageLeftMargin, PageRightMargin) с помощью[**PrintProps**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops)члены класса. Ниже перечислены несколько методов, которые используются для указания полей страницы:

- [**PageTopMargin**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/pagetopmargin)
- [**СтраницаНижняяПоля**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/pagebottommargin)
- [**PageLeftMargin**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/pageleftmargin)
- [**PageRightMargin**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/pagerightmargin)

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-SetPageMargin-SetPageMargin.cs" >}}