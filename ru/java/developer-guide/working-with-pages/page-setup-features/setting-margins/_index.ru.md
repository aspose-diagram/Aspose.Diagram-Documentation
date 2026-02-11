---
title: Настройка полей
type: docs
weight: 20
url: /ru/java/setting-margins/
description: В этом разделе объясняется, как установить параметры страницы visio с помощью Aspose.Diagram.
---
{{% alert color="primary" %}}

Aspose.Diagram полностью поддерживает параметры настройки страницы Microsoft Visio. Разработчикам может потребоваться настроить параметры страницы для управления процессом печати. В этом разделе обсуждается, как использовать Aspose.Diagram для настройки полей страницы.

{{% /alert %}}

## **Настройка полей**

 Aspose.Diagram предоставляет класс,[**Страница**](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) , представляющий файл Microsoft Visio.[**Diagram**](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) класс содержит[**Страницы**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagecollection) коллекция, которая позволяет получить доступ к каждой странице в файле Visio. Страница представлена[**Страница**](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)учебный класс.

[**СтраницаЛист**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet) класс обеспечивает[**PrintProps**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps) свойство, которое используется для установки параметров настройки страницы. На самом деле это[**PrintProps**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps) имущество – это объект[**СтраницаЛист**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet) класс, используемый для установки различных параметров макета страницы для печатной страницы.[**PrintProps**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps)Класс предоставляет различные свойства, используемые для установки параметров настройки страницы. Некоторые из этих свойств обсуждаются ниже.

### **Поля страницы**

 Установите поля страницы (PageTopMargin, PageBottomMargin, PageLeftMargin, PageRightMargin) с помощью[**PrintProps**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps)члены класса. Ниже перечислены несколько методов, которые используются для указания полей страницы:

- [**PageTopMargin**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#PageTopMargin)
- [**СтраницаНижняяПоля**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#PageBottomMargin)
- [**PageLeftMargin**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#PageLeftMargin)
- [**PageRightMargin**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#PageRightMargin)


```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(Test.class);

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

//Set Page Margin
diagram.getPages().get(0).getPageSheet().getPrintProps().getPageLeftMargin().setValue( 0.01);
diagram.getPages().get(0).getPageSheet().getPrintProps().getPageRightMargin().setValue( 0.01);
diagram.getPages().get(0).getPageSheet().getPrintProps().getPageTopMargin().setValue( 0.01);
diagram.getPages().get(0).getPageSheet().getPrintProps().getPageBottomMargin().setValue( 0.01);
{{< /highlight >}}
```