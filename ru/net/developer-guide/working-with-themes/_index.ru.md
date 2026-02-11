---
title: Работа с темами
type: docs
weight: 265
url: /ru/net/working-with-themes/
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
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioThemes();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Themes1.vsdx");
//Get an instance of Page class to be set theme
Page page = diagram.Pages[0];
//Assign a Preset value to the PresetTheme property of the Page instance
page.PresetTheme = PresetThemeValue.Bubble;
// Save diagram
diagram.Save(dataDir + "SetTheme_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```

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

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioThemes();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Themes1.vsdx");
//Get an instance of Page class to be set theme
Page page = diagram.Pages[0];
//Assign a Preset value to the PresetTheme property of the Page instance
page.PresetTheme = PresetThemeValue.Bubble;
//Assign a Preset value to the PresetThemeVariant property of the Page instance
page.PresetThemeVariant = PresetThemeVariantValue.Variant3;
// Save diagram
diagram.Save(dataDir + "SetTheme_out.vsdx", SaveFileFormat.VSDX);
{{< /highlight >}}
```

|**Результат применения предустановленного варианта темы к странице**|
|:- |
|![SetTheme_out.vsdx](theme3.png)|

### **Применение предустановленной темы к фигуре**

Aspose.Diagram API позволяет применять предустановленную тему к фигуре на странице. Для этого выполните следующие шаги:

- Создайте экземпляр класса Diagram для загрузки diagram
- Получить экземпляр класса Shape для установки темы
- Назначьте значение Preset свойству PresetTheme экземпляра Shape.

#### **Применение предустановленной темы к образцу программирования формы**

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioThemes();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Themes1.vsdx");
//Get an instance of Shape class to be set theme
Shape shape = doc.Pages[0].Shapes[0];
//Assign a Preset value to the PresetTheme property of the Shape instance
shape.PresetTheme = PresetThemeValue.Bubble;
// Save diagram
diagram.Save(dataDir + "SetTheme_out.vsdx", SaveFileFormat.VSDX);
{{< /highlight >}}
```

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

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioThemes();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Themes1.vsdx");
//Get an instance of Shape class to be set theme
Shape shape = doc.Pages[0].Shapes[0];
//Assign a Preset value to the PresetTheme property of the Shape instance
shape.PresetTheme = PresetThemeValue.Bubble;
//Assign a Preset value to the PresetThemeVariant property of the Shape instance
shape.PresetThemeVariant = PresetThemeVariantValue.Variant3;
// Save diagram
diagram.Save(dataDir + "SetTheme_out.vsdx", SaveFileFormat.VSDX);
{{< /highlight >}}
```

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

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioThemes();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Themes1.vsdx");
//Get an instance of Shape class to be set theme
Shape shape = doc.Pages[0].Shapes[0];
//Assign a Preset value to the PresetTheme property of the Shape instance
shape.PresetTheme = PresetThemeValue.Bubble;
//Assign a Preset value to the PresetThemeVariant property of the Shape instance
shape.PresetThemeVariant = PresetThemeVariantValue.Variant3;
//Assign a Preset value to the PresetThemeQuickStyle property of the Shape instance
shape.PresetThemeQuickStyle = PresetQuickStyleValue.VariantStyle2;
// Save diagram
diagram.Save(dataDir + "SetTheme_out.vsdx", SaveFileFormat.VSDX);
{{< /highlight >}}
```

|**Результат применения предварительно заданного варианта темы Quickstyle к фигуре**|
|:- |
|![SetTheme_out.vsdx](theme6.png)|

### **Применение предустановленного стиля темы к фигуре с помощью метода SetPresetThemeStyleMatrics**

Aspose.Diagram API позволяет применять готовый быстрый стиль темы к фигуре на странице. Для этого выполните следующие шаги:

- Создайте экземпляр класса Diagram для загрузки diagram
- Получить экземпляр класса Shape для установки темы
- Назначьте значение Preset свойству PresetTheme экземпляра Shape.
- Назначьте значение Preset свойству PresetThemeVariant экземпляра Shape.
- Назначьте стиль темы, установив значение стиля и значение цвета экземпляра Shape с помощью метода SetPresetThemeStyleMatrics.

#### **Применение предустановленного стиля темы к фигуре с помощью примера программирования метода SetPresetThemeStyleMatrics**

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioThemes();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Themes1.vsdx");
//Get an instance of Shape class to be set theme
Shape shape = doc.Pages[0].Shapes[0];
//Assign a Preset value to the PresetTheme property of the Shape instance
shape.PresetTheme = PresetThemeValue.Bubble;
//Assign a Preset value to the PresetThemeVariant property of the Shape instance
shape.PresetThemeVariant = PresetThemeVariantValue.Variant3;
//Assign a theme style by setting style value and color value of the Shape instance
shape.SetPresetThemeStyleMatrics(PresetStyleMatricsValue.Style2, PresetColorMatricsValue.Color7);
// Save diagram
diagram.Save(dataDir + "SetTheme_out.vsdx", SaveFileFormat.VSDX);
{{< /highlight >}}
```

|**Результат применения предустановленного стиля темы к фигуре с использованием метода SetPresetThemeStyleMatrics**|
|:- |
|![SetTheme_out.vsdx](theme7.png)|
