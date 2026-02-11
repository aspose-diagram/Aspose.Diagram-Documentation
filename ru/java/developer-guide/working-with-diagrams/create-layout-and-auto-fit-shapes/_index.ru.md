---
title: Создание, компоновка и автоматическая подгонка фигур
type: docs
weight: 10
url: /ru/java/create-layout-and-auto-fit-shapes/
---
## **Создание Diagram**
 Aspose.Diagram for Java позволяет читать и создавать Microsoft Visio диаграммы из ваших собственных приложений без автоматизации. Первым шагом при создании новых документов является создание diagram. Затем[добавить фигуры и соединители](/diagram/ru/java/add-and-connect-visio-shapes/)для создания diagram. Используйте конструктор по умолчанию[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) класс для создания нового diagram.
### **Образец программирования**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CreateDiagram.class);
// Create directory if it is not already present.
File file = new File(dataDir);
if (!file.exists())
	file.mkdir();
// initialize a new Diagram
Diagram diagram = new Diagram();
// save in the VSDX format
diagram.save(dataDir + "CreateDiagram_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Формы макета в стиле блок-схемы**
 С определенными типами подключенных чертежей, такими как блок-схемы и сетевые диаграммы, вы можете использовать**Формы макета** функция автоматического позиционирования фигур. Автоматическое позиционирование выполняется быстрее, чем ручное перетаскивание каждой фигуры в новое место.

Например, если вы обновляете большую блок-схему, чтобы включить новый процесс, вы можете добавить и соединить фигуры, составляющие процесс, а затем использовать функцию макета для автоматического макета обновленного рисунка.

 Метод Layout, представленный[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) class размещает фигуры и/или перенаправляет соединители на всех страницах diagram. Этот метод принимает объект LayoutOptions в качестве аргумента. Используйте различные свойства, предоставляемые классом LayoutOptions, для автоматического размещения фигур.

На изображении ниже показан код diagram, загруженный фрагментами кода в этой статье, до применения автоматического макета. Фрагменты кода показывают, как подать заявку[макеты блок-схем](/diagram/ru/java/create-2c-layout-and-auto-fit-shapes/) а также[компактные макеты дерева](/diagram/ru/java/create-2c-layout-and-auto-fit-shapes/).

**Источник diagram.** 

![дело:изображение_альтернативный_текст](create-layout-and-auto-fit-shapes_1.png)

Фрагменты кода в этой статье берут исходный код diagram и применяют к нему несколько типов автоматической разметки, сохраняя каждый в отдельном файле.

|<p>**Формы макета снизу вверх** </p><p>![дело:изображение_альтернативный_текст](create-layout-and-auto-fit-shapes_2.png)</p>|<p>**Формы макета сверху вниз** </p><p>![дело:изображение_альтернативный_текст](create-layout-and-auto-fit-shapes_3.png)</p>|
|:- |:- |
|<p>**Формы макета слева направо** </p><p>![дело:изображение_альтернативный_текст](create-layout-and-auto-fit-shapes_4.png)</p>|<p>**Формы макета справа налево** </p><p>![дело:изображение_альтернативный_текст](create-layout-and-auto-fit-shapes_5.png)</p>|
Чтобы разместить фигуры в стиле блок-схемы:

1. Создайте экземпляр класса Diagram.
1. Создайте экземпляр класса LayoutOptions и задайте свойства, связанные со стилем блок-схемы.
1. Вызовите метод Layout класса Diagram, передав LayoutOptions.
1. Вызовите метод Save класса Diagram, чтобы записать рисунок Visio.
### **Пример программирования в стиле блок-схемы**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(LayOutShapesInFlowchartStyle.class);     

// load an existing Visio diagram
String fileName = "LayOutShapesInFlowchartStyle.vdx";
Diagram diagram = new Diagram(dataDir + fileName);

// set layout options 
LayoutOptions flowChartOptions = new LayoutOptions();
flowChartOptions.setLayoutStyle(LayoutStyle.FLOW_CHART);
flowChartOptions.setSpaceShapes(1f);
flowChartOptions.setEnlargePage(true);

// set layout direction as BottomToTop and then save
flowChartOptions.setDirection(LayoutDirection.BOTTOM_TO_TOP);
diagram.layout(flowChartOptions);
diagram.save(dataDir + "sample_btm_top.vdx", SaveFileFormat.VDX);

// set layout direction as TopToBottom and then save
diagram = new Diagram(dataDir + fileName);
flowChartOptions.setDirection(LayoutDirection.TOP_TO_BOTTOM);
diagram.layout(flowChartOptions);
diagram.save(dataDir + "sample_top_btm.vdx", SaveFileFormat.VDX);

// set layout direction as LeftToRight and then save
diagram = new Diagram(dataDir + fileName);
flowChartOptions.setDirection(LayoutDirection.LEFT_TO_RIGHT);
diagram.layout(flowChartOptions);
diagram.save(dataDir + "sample_left_right.vdx", SaveFileFormat.VDX);

// set layout direction as RightToLeft and then save
diagram = new Diagram(dataDir + fileName);
flowChartOptions.setDirection(LayoutDirection.RIGHT_TO_LEFT);
diagram.layout(flowChartOptions);
diagram.save(dataDir + "sample_right_left.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
### **Размещение фигур в стиле компактного дерева**
 Компактный стиль компоновки дерева пытается построить древовидную структуру. Он использует тот же входной файл, что и[пример выше](/diagram/ru/java/create-2c-layout-and-auto-fit-shapes/)и сохраняет в несколько различных стилей компактного дерева.

|<p>**Компактное древовидное расположение — вниз и вправо** </p><p>![дело:изображение_альтернативный_текст](create-layout-and-auto-fit-shapes_6.png)</p>|
|:- |
|<p>**Компактное древовидное расположение — вниз и влево** </p><p>![дело:изображение_альтернативный_текст](create-layout-and-auto-fit-shapes_7.png)</p>|


|<p>**Компактная древовидная компоновка - справа и снизу** </p><p>![дело:изображение_альтернативный_текст](create-layout-and-auto-fit-shapes_8.png)</p>|<p>**Компактное древовидное расположение — слева и снизу** </p><p>![дело:изображение_альтернативный_текст](create-layout-and-auto-fit-shapes_9.png)</p>|
|:- |:- |
Чтобы разместить фигуры в компактном древовидном стиле:

1.  Создайте экземпляр[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) учебный класс.
1. Создайте экземпляр класса LayoutOptions и задайте свойства стиля компактного дерева.
1. Вызовите метод Layout класса Diagram, передав LayoutOptions.
1. Вызовите метод Save класса Diagram, чтобы записать файл Visio.
#### **Пример программирования в стиле компактного дерева**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(LayOutShapesInCompactTreeStyle.class);
        
String fileName = "LayOutShapesInCompactTreeStyle.vdx";
// load an existing Visio diagram
Diagram diagram = new Diagram(dataDir + fileName);

// set layout options 
LayoutOptions compactTreeOptions = new LayoutOptions();
compactTreeOptions.setLayoutStyle(LayoutStyle.COMPACT_TREE);
compactTreeOptions.setEnlargePage(true);

// set layout direction as DownThenRight and then save
compactTreeOptions.setDirection(LayoutDirection.DOWN_THEN_RIGHT);
diagram.layout(compactTreeOptions);
diagram.save(dataDir + "sample_down_right.vdx", SaveFileFormat.VDX);

// set layout direction as DownThenLeft and then save
diagram = new Diagram(dataDir + fileName);
compactTreeOptions.setDirection(LayoutDirection.DOWN_THEN_LEFT);
diagram.layout(compactTreeOptions);
diagram.save(dataDir + "sample_down_left.vdx", SaveFileFormat.VDX);

// set layout direction as RightThenDown and then save
diagram = new Diagram(dataDir + fileName);
compactTreeOptions.setDirection(LayoutDirection.RIGHT_THEN_DOWN);
diagram.layout(compactTreeOptions);
diagram.save(dataDir + "sample_right_down.vdx", SaveFileFormat.VDX);

// set layout direction as LeftThenDown and then save
diagram = new Diagram(dataDir + fileName);
compactTreeOptions.setDirection(LayoutDirection.LEFT_THEN_DOWN);
diagram.layout(compactTreeOptions);
diagram.save(dataDir + "sample_left_down.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
## **Автоматическая установка Visio Diagram**
Aspose.Diagram API поддерживает автоматическую подгонку чертежа Visio. Эта функция помогает помещать внешние фигуры внутрь границ страницы Visio.

Aspose.Diagram for Java API имеет класс Diagram, представляющий чертеж Visio. Класс DiagramSaveOptions предоставляет свойство AutoFitPageToDrawingContent для автоматического подбора чертежа Visio.

Этот пример работает следующим образом:

1. Создайте объект класса Diagram.
1. Создайте объект класса DiagramSaveOptions и передайте результирующий формат файла.
1. Установите свойство AutoFitPageToDrawingContent объекта DiagramSaveOptions.
1. Вызовите метод Save объекта класса Diagram, а также передайте полный путь к файлу и объект DiagramSaveOptions.
### **Пример программирования автоматической подгонки**
В следующем примере кода показано, как автоматически подгонять фигуры в Visio diagram.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AutoFitShapesInVisio.class);
// load a Visio diagram
Diagram diagram = new Diagram(dataDir + "BFlowcht.vsdx");

// use saving options
DiagramSaveOptions options = new DiagramSaveOptions(SaveFileFormat.VSDX);
// set Auto fit page property
options.setAutoFitPageToDrawingContent(true);

// save Visio diagram
diagram.save(dataDir + "AutoFitShapesInVisio_Out.vsdx", options);

{{< /highlight >}}
```
## **Работа с проектом VBA**
### **Изменить код модуля VBA в Visio Diagram**
В этой статье показано, как автоматически изменить код модуля VBA с помощью Aspose.Diagram for Java.

Мы добавили классы VbaModule, VbaModuleCollection, VbaProject, VbaProjectReference и VbaProjectReferenceCollection. Эти классы помогают получить контроль над проектом VBA. Разработчики могут извлекать и изменять код модуля VBA.
### **Изменить пример программирования кода модуля VBA**
Пожалуйста, проверьте этот пример кода:

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// load an existing Visio diagram
String dataDir = Utils.getDataDir(ModifyVBAModuleCode.class);
InputStream input = new FileInputStream(dataDir + "macro.vsdm");
Diagram diagram = new Diagram(input);
// extract VBA project
VbaProject v = diagram.getVbaProject();
// Iterate through the modules and modify VBA macro code
for (int i = 0; i < diagram.getVbaProject().getModules().getCount(); i++) {
	VbaModule module = diagram.getVbaProject().getModules().get(i);
	String code = module.getCodes();
	if (code.contains("This is test message."))
		code = code.replace("This is test message.", "This is Aspose.Diagram message.");
	module.setCodes(code);
}
// save the Visio diagram
diagram.save(dataDir + "out.vssm", SaveFileFormat.VSSM);

{{< /highlight >}}
```
### **Удалить все макросы из Visio Diagram**
Aspose.Diagram for Java позволяет разработчикам удалить все макросы из файла Visio diagram.

Свойство JavaProjectData, предоставляемое[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) class, позволяет удалить все макросы из чертежа Visio.
### **Пример программирования удаления всех макросов**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RemoveMacrosFromVisio.class);  
// load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// remove all macros
diagram.setVbProjectData(null);

// Save diagram
diagram.save(dataDir + "RemoveMacrosFromVisio_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
