---
title: Настройка параметров печати
type: docs
weight: 10
url: /ru/java/setting-print-options/
description: В этом разделе объясняется, как установить параметры печати с помощью Aspose.Diagram.
---
{{% alert color="primary" %}}

Иногда необходимо настроить параметры страницы для управления печатью. Эти параметры настройки страницы предлагают различные варианты.

{{% /alert %}}

## **Настройка параметров печати**

Параметры настройки страницы полностью поддерживаются в Aspose.Diagram. В этой статье объясняется, как установить параметры страницы с помощью Aspose.Diagram, и показаны примеры кода для настройки:

 Aspose.Diagram предоставляет класс,[**Страница**](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) , представляющий файл Microsoft Visio.[**Diagram**](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) класс содержит[**Страницы**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagecollection) коллекция, которая позволяет получить доступ к каждой странице в файле Visio. Страница представлена[**Страница**](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)учебный класс.

[**СтраницаЛист**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet) класс обеспечивает[**PrintProps**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps) свойство, которое используется для установки параметров настройки страницы. На самом деле это[**PrintProps**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps) имущество – это объект[**СтраницаЛист**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet) класс, используемый для установки различных параметров макета страницы для печатной страницы.[**PrintProps**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps)Класс предоставляет различные свойства, используемые для установки параметров настройки страницы. Некоторые из этих свойств обсуждаются ниже.

### **Ориентация страницы печати**

 Ориентация страницы печати может быть установлена на книжную или альбомную с помощью[**PrintProps**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps) учебный класс'[**PrintPageOrientation**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#PrintPageOrientation) имущество.[**PrintPageOrientation**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#PrintPageOrientation) свойство принимает одно из предопределенных значений в[**Принтпажеориентатионвалуе**](https://reference.aspose.com/diagram/java/com.aspose.diagram/PrintPageOrientationValue)перечисление, приведенное ниже.

|**Типы ориентации страницы печати**|**Описание**|
|:- |:- |
|Самеаспринтер|То же, что и ориентация принтера|
|Пейзаж|Альбомная ориентация|
|Портрет|Портретная ориентация|

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Print-SetPageOrientation-SetPageOrientation.java" >}}

### **Коэффициент масштабирования**

 Можно уменьшить или увеличить размер страницы, отрегулировав коэффициент масштабирования с помощью[**МасштабX**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#ScaleX)имущество.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Print-SetPageOrientation-SetPageScale.java" >}}
