﻿---
title: Работа с темами
type: docs
weight: 265
url: /ru/java/working-with-themes/
description: В этом разделе объясняется, как применить предустановленную тему к странице или фигуре с помощью Aspose.Diagram.
---
## **Как применить предустановленную тему к странице или фигуре**
Эта статья может быть полезна всем, кто хочет модифицировать тему дающего файла VSDX с помощью Aspose.Diagram. Мы используем тестовый файл Themes1.vsdx, как показано ниже.

|**Тема1.vsdx**|
|:- |
|![Тема1.vsdx](theme1.png)|

### **Применение предустановленной темы к странице**
Aspose.Diagram API-интерфейсы позволяют применять предустановленную тему для получения единообразного внешнего вида фигур на странице и в нескольких документах. Для этого выполните следующие шаги:

- Создайте экземпляр класса Diagram для загрузки diagram
- Получить экземпляр класса Page для установки темы
- Назначьте значение Preset свойству PresetTheme экземпляра страницы.
#### **Применение предустановленной темы к образцу программирования страницы**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Working-with-Theme-SetThemeForPage.java" >}}

|**Результат применения предустановленной темы к странице**|
|:- |
|![SetTheme_out.vsdx](theme2.png)|

### **Применение предустановленного варианта темы к странице**

Aspose.Diagram API-интерфейсы позволяют применять предустановленный вариант темы, чтобы получить единый внешний вид фигур на странице и в нескольких документах. Для этого выполните следующие шаги:

- Создайте экземпляр класса Diagram для загрузки diagram
- Получить экземпляр класса Page для установки темы
- Назначьте значение Preset свойству PresetTheme экземпляра страницы.
- Присвойте значение Preset свойству PresetThemeVariant экземпляра Page.

#### **Применение предустановленного варианта темы к образцу программирования страницы**

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Working-with-Theme-SetThemeVariantForPage.java" >}}

|**Результат применения предустановленного варианта темы к странице**|
|:- |
|![SetTheme_out.vsdx](theme3.png)|

### **Применение предустановленной темы к фигуре**

Aspose.Diagram API позволяет применять предустановленную тему к фигуре на странице. Для этого выполните следующие шаги:

- Создайте экземпляр класса Diagram для загрузки diagram
- Получить экземпляр класса Shape для установки темы
- Назначьте значение Preset свойству PresetTheme экземпляра Shape.

#### **Применение предустановленной темы к образцу программирования формы**

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Working-with-Theme-SetThemeForShape.java" >}}

|**Результат применения предустановленной темы к фигуре**|
|:- |
|![SetTheme_out.vsdx](theme4.png)|

### **Применение предустановленного варианта темы к фигуре**

Aspose.Diagram API позволяет применить предустановленный вариант темы к фигуре на странице. Для этого выполните следующие шаги:

- Создайте экземпляр класса Diagram для загрузки diagram
- Получить экземпляр класса Shape для установки темы
- Назначьте значение Preset свойству PresetTheme экземпляра Shape.
- Назначьте значение Preset свойству PresetThemeVariant экземпляра Shape.

#### **Применение предустановленного варианта темы к образцу программирования формы**

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Working-with-Theme-SetThemeVariantForShape.java" >}}

|**Результат применения предустановленного варианта темы к фигуре**|
|:- |
|![SetTheme_out.vsdx](theme5.png)|

### **Применение предварительно заданного варианта темы Quickstyle к фигуре**

Aspose.Diagram API позволяет применять готовый быстрый стиль темы к фигуре на странице. Для этого выполните следующие шаги:

- Создайте экземпляр класса Diagram для загрузки diagram
- Получить экземпляр класса Shape для установки темы
- Назначьте значение Preset свойству PresetTheme экземпляра Shape.
- Назначьте значение Preset свойству PresetThemeVariant экземпляра Shape.
- Назначьте значение Preset свойству PresetThemeQuickStyle экземпляра Shape.

#### **Применение предварительно заданного варианта темы Quickstyle к образцу программирования формы**

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Working-with-Theme-SetThemeQuickStyleForShape.java" >}}

|**Результат применения предварительно заданного варианта темы Quickstyle к фигуре**|
|:- |
|![SetTheme_out.vsdx](theme6.png)|

### **Применение предустановленного стиля темы к фигуре с помощью метода SetPresetThemeStyleMatrics**

Aspose.Diagram API позволяет применять готовый быстрый стиль темы к фигуре на странице. Для этого выполните следующие шаги:

- Создайте экземпляр класса Diagram для загрузки diagram
- Получить экземпляр класса Shape для установки темы
- Назначьте значение Preset свойству PresetTheme экземпляра Shape.
- Назначьте значение Preset свойству PresetThemeVariant экземпляра Shape.
- Назначьте стиль темы, установив значение стиля и значение цвета экземпляра Shape с помощью метода setPresetThemeStyleMatrics.

#### **Применение предустановленного стиля темы к фигуре с помощью примера программирования метода setPresetThemeStyleMatrics**

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Working-with-Theme-SetThemeStyleMatricsForShape.java" >}}

|**Результат применения предустановленного стиля темы к фигуре с использованием метода setPresetThemeStyleMatrics** |
|:----------------------------------------------------------- |
|![SetTheme_out.vsdx](theme7.png)                             |