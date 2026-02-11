---
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

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(VisioThemes.class);
// Load diagram
Diagram diagram = new Diagram(dataDir + "Themes1.vsdx");
//Get an instance of Page class to be set theme
Page page = diagram.getPages().get(0);
//Assign a Preset value to the PresetTheme property of the Page instance
page.setPresetTheme(PresetThemeValue.BUBBLE);
// Save diagram
diagram.save(dataDir + "SetTheme_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


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


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(VisioThemes.class);
// Load diagram
Diagram diagram = new Diagram(dataDir + "Themes1.vsdx");
//Get an instance of Page class to be set theme
Page page = diagram.getPages().get(0);
//Assign a Preset value to the PresetTheme property of the Page instance
page.setPresetTheme(PresetThemeValue.BUBBLE);
//Assign a Preset value to the PresetThemeVariant property of the Page instance
page.setPresetThemeVariant(PresetThemeVariantValue.VARIANT_3);
// Save diagram
diagram.save(dataDir + "SetTheme_out.vsdx", SaveFileFormat.VSDX);
{{< /highlight >}}


|**Результат применения предустановленного варианта темы к странице**|
|:- |
|![SetTheme_out.vsdx](theme3.png)|

### **Применение предустановленной темы к фигуре**

Aspose.Diagram API позволяет применять предустановленную тему к фигуре на странице. Для этого выполните следующие шаги:

- Создайте экземпляр класса Diagram для загрузки diagram
- Получить экземпляр класса Shape для установки темы
- Назначьте значение Preset свойству PresetTheme экземпляра Shape.

#### **Применение предустановленной темы к образцу программирования формы**


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(VisioThemes.class);
// Load diagram
Diagram diagram = new Diagram(dataDir + "Themes1.vsdx");
//Get an instance of Shape class to be set theme
Shape shape = doc.getPages().get(0).getShapes().get(0);
//Assign a Preset value to the PresetTheme property of the Shape instance
shape.setPresetTheme(PresetThemeValue.BUBBLE);
// Save diagram
diagram.save(dataDir + "SetTheme_out.vsdx", SaveFileFormat.VSDX);
{{< /highlight >}}


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


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(VisioThemes.class);
// Load diagram
Diagram diagram = new Diagram(dataDir + "Themes1.vsdx");
//Get an instance of Shape class to be set theme
Shape shape = doc.getPages().get(0).getShapes().get(0);
//Assign a Preset value to the PresetTheme property of the Shape instance
shape.setPresetTheme(PresetThemeValue.BUBBLE);
//Assign a Preset value to the PresetThemeVariant property of the Shape instance
shape.setPresetThemeVariant(PresetThemeVariantValue.VARIANT_3);
// Save diagram
diagram.save(dataDir + "SetTheme_out.vsdx", SaveFileFormat.VSDX);
{{< /highlight >}}


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


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(VisioThemes.class);
// Load diagram
Diagram diagram = new Diagram(dataDir + "Themes1.vsdx");
//Get an instance of Shape class to be set theme
Shape shape = doc.getPages().get(0).getShapes().get(0);
//Assign a Preset value to the PresetTheme property of the Shape instance
shape.setPresetTheme(PresetThemeValue.BUBBLE);
//Assign a Preset value to the PresetThemeVariant property of the Shape instance
shape.setPresetThemeVariant(PresetThemeVariantValue.VARIANT_3);
//Assign a Preset value to the PresetThemeQuickStyle property of the Shape instance
shape.setPresetThemeQuickStyle(PresetQuickStyleValue.VARIANT_STYLE_2);
// Save diagram
diagram.save(dataDir + "SetTheme_out.vsdx", SaveFileFormat.VSDX);
{{< /highlight >}}


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


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(VisioThemes.class);
// Load diagram
Diagram diagram = new Diagram(dataDir + "Themes1.vsdx");
//Get an instance of Shape class to be set theme
Shape shape = doc.getPages().get(0).getShapes().get(0);
//Assign a Preset value to the PresetTheme property of the Shape instance
shape.setPresetTheme(PresetThemeValue.BUBBLE);
//Assign a Preset value to the PresetThemeVariant property of the Shape instance
shape.setPresetThemeVariant(PresetThemeVariantValue.VARIANT_3);
//Assign a theme style by setting style value and color value of the Shape instance
shape.setPresetThemeStyleMatrics(PresetStyleMatricsValue.STYLE_2, PresetColorMatricsValue.COLOR_7);
// Save diagram
diagram.save(dataDir + "SetTheme_out.vsdx", SaveFileFormat.VSDX);
{{< /highlight >}}


|**Результат применения предустановленного стиля темы к фигуре с использованием метода setPresetThemeStyleMatrics** |
|:----------------------------------------------------------- |
|![SetTheme_out.vsdx](theme7.png)                             |
