---
title: Создание, компоновка и автоматическая подгонка фигур
type: docs
weight: 10
url: /ru/python-java/create-layout-and-auto-fit-shapes/
---
## **Создание Diagram**
 Aspose.Diagram для Python via Java позволяет читать и создавать Microsoft Visio схемы из ваших собственных приложений без автоматизации. Первым шагом при создании новых документов является создание diagram. Затем[добавить фигуры и соединители](/diagram/ru/python-java/add-and-connect-visio-shapes/) для создания diagram. Используйте конструктор по умолчанию класса Diagram, чтобы создать новый diagram.
### **Образец программирования**
```
{{< highlight "python" >}}
import jpype
import os
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# initialize a new Diagram
diagram = Diagram()
# save in the VSDX format
diagram.save("CreateDiagram_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}
```
## **Формы макета в стиле блок-схемы**
 С определенными типами подключенных чертежей, такими как блок-схемы и сетевые диаграммы, вы можете использовать**Формы макета** функция автоматического позиционирования фигур. Автоматическое позиционирование выполняется быстрее, чем ручное перетаскивание каждой фигуры в новое место.

Например, если вы обновляете большую блок-схему, чтобы включить новый процесс, вы можете добавить и соединить фигуры, составляющие процесс, а затем использовать функцию макета для автоматического макета обновленного рисунка.

Метод Layout, предоставляемый классом Diagram, размещает фигуры и/или перенаправляет соединители на всех страницах diagram. Этот метод принимает объект LayoutOptions в качестве аргумента. Используйте различные свойства, предоставляемые классом LayoutOptions, для автоматического размещения фигур.

На изображении ниже показан код diagram, загруженный фрагментами кода в этой статье, до применения автоматического макета. Фрагменты кода показывают, как применять макеты блок-схем и компактные макеты дерева.

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
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load an existing Visio diagram
fileName = "LayOutShapesInFlowchartStyle.vdx"
diagram = Diagram(fileName)

# set layout options
flowChartOptions = LayoutOptions()
flowChartOptions.setLayoutStyle(LayoutStyle.FLOW_CHART)
flowChartOptions.setSpaceShapes(1)
flowChartOptions.setEnlargePage(True)

# set layout direction as BottomToTop and then save
flowChartOptions.setDirection(LayoutDirection.BOTTOM_TO_TOP)
diagram.layout(flowChartOptions)
diagram.save("sample_btm_top.vdx", SaveFileFormat.VDX)

# set layout direction as TopToBottom and then save
diagram = Diagram(fileName)
flowChartOptions.setDirection(LayoutDirection.TOP_TO_BOTTOM)
diagram.layout(flowChartOptions)
diagram.save("sample_top_btm.vdx", SaveFileFormat.VDX)

# set layout direction as LeftToRight and then save
diagram = Diagram(fileName)
flowChartOptions.setDirection(LayoutDirection.LEFT_TO_RIGHT)
diagram.layout(flowChartOptions)
diagram.save("sample_left_right.vdx", SaveFileFormat.VDX)

# set layout direction as RightToLeft and then save
diagram = Diagram(fileName)
flowChartOptions.setDirection(LayoutDirection.RIGHT_TO_LEFT)
diagram.layout(flowChartOptions)
diagram.save("sample_right_left.vdx", SaveFileFormat.VDX)

jpype.shutdownJVM()

{{< /highlight >}}
```
### **Размещение фигур в стиле компактного дерева**
Компактный стиль компоновки дерева пытается построить древовидную структуру. Он использует тот же входной файл, что и в приведенном выше примере, и сохраняет его в нескольких различных стилях компактного дерева.

|<p>**Компактное древовидное расположение — вниз и вправо** </p><p>![дело:изображение_альтернативный_текст](create-layout-and-auto-fit-shapes_6.png)</p>|
|:- |
|<p>**Компактное древовидное расположение — вниз и влево** </p><p>![дело:изображение_альтернативный_текст](create-layout-and-auto-fit-shapes_7.png)</p>|


|<p>**Компактная древовидная компоновка - справа и снизу** </p><p>![дело:изображение_альтернативный_текст](create-layout-and-auto-fit-shapes_8.png)</p>|<p>**Компактное древовидное расположение — слева и снизу** </p><p>![дело:изображение_альтернативный_текст](create-layout-and-auto-fit-shapes_9.png)</p>|
|:- |:- |
Чтобы разместить фигуры в компактном древовидном стиле:

1. Создайте экземпляр класса Diagram.
1. Создайте экземпляр класса LayoutOptions и задайте свойства стиля компактного дерева.
1. Вызовите метод Layout класса Diagram, передав LayoutOptions.
1. Вызовите метод Save класса Diagram, чтобы записать файл Visio.
#### **Пример программирования в стиле компактного дерева**
```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

        
fileName = "LayOutShapesInCompactTreeStyle.vdx"
# load an existing Visio diagram
diagram = Diagram(fileName)

# set layout options 
compactTreeOptions = LayoutOptions()
compactTreeOptions.setLayoutStyle(LayoutStyle.COMPACT_TREE)
compactTreeOptions.setEnlargePage(True)

# set layout direction as DownThenRight and then save
compactTreeOptions.setDirection(LayoutDirection.DOWN_THEN_RIGHT)
diagram.layout(compactTreeOptions)
diagram.save("sample_down_right.vdx", SaveFileFormat.VDX)

# set layout direction as DownThenLeft and then save
diagram = Diagram(fileName)
compactTreeOptions.setDirection(LayoutDirection.DOWN_THEN_LEFT)
diagram.layout(compactTreeOptions)
diagram.save("sample_down_left.vdx", SaveFileFormat.VDX)

# set layout direction as RightThenDown and then save
diagram = Diagram(fileName)
compactTreeOptions.setDirection(LayoutDirection.RIGHT_THEN_DOWN)
diagram.layout(compactTreeOptions)
diagram.save("sample_right_down.vdx", SaveFileFormat.VDX)

# set layout direction as LeftThenDown and then save
diagram = Diagram(fileName)
compactTreeOptions.setDirection(LayoutDirection.LEFT_THEN_DOWN)
diagram.layout(compactTreeOptions)
diagram.save("sample_left_down.vdx", SaveFileFormat.VDX)

jpype.shutdownJVM()

{{< /highlight >}}
```
## **Автоматическая установка Visio Diagram**
Aspose.Diagram API поддерживает автоматическую подгонку чертежа Visio. Эта функция помогает помещать внешние фигуры внутрь границ страницы Visio.

Aspose.Diagram для Python via Java API имеет класс Diagram, который представляет чертеж Visio. Класс DiagramSaveOptions предоставляет свойство AutoFitPageToDrawingContent для автоматического подбора чертежа Visio.

Этот пример работает следующим образом:

1. Создайте объект класса Diagram.
1. Создайте объект класса DiagramSaveOptions и передайте результирующий формат файла.
1. Установите свойство AutoFitPageToDrawingContent объекта DiagramSaveOptions.
1. Вызовите метод Save объекта класса Diagram, а также передайте полный путь к файлу и объект DiagramSaveOptions.
### **Пример программирования автоматической подгонки**
В следующем примере кода показано, как автоматически подгонять фигуры в Visio diagram.

```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load a Visio diagram
diagram = Diagram("BFlowcht.vsdx")

# use saving options
options = DiagramSaveOptions(SaveFileFormat.VSDX)
# set Auto fit page property
options.setAutoFitPageToDrawingContent(True)

# save Visio diagram
diagram.save("AutoFitShapesInVisio_Out.vsdx", options)

jpype.shutdownJVM()

{{< /highlight >}}
```
## **Работа с проектом VBA**
### **Изменить код модуля VBA в Visio Diagram**
В этой статье показано, как автоматически изменить код модуля VBA, используя Aspose.Diagram для Python via Java.

Мы добавили классы VbaModule, VbaModuleCollection, VbaProject, VbaProjectReference и VbaProjectReferenceCollection. Эти классы помогают получить контроль над проектом VBA. Разработчики могут извлекать и изменять код модуля VBA.
### **Изменить пример программирования кода модуля VBA**
Пожалуйста, проверьте этот пример кода:

```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

diagram = Diagram("Macro.vsdm")
# extract VBA project
v = diagram.getVbaProject()
# Iterate through the modules and modify VBA macro code
for i in range(0, diagram.getVbaProject().getModules().getCount() - 1):
	module = diagram.getVbaProject().getModules().get(i)
	code = module.getCodes()
	if code.contains("This is test message."):
		code = code.replace("This is test message.", "This is Aspose.Diagram message.")
	module.setCodes(code)

# save the Visio diagram
diagram.save("out.vssm", SaveFileFormat.VSSM)

jpype.shutdownJVM()

{{< /highlight >}}
```
### **Удалить все макросы из Visio Diagram**
Aspose.Diagram для Python via Java позволяет разработчикам удалить все макросы из файла Visio diagram.

Свойство JavaProjectData, предоставляемое классом Diagram, позволяет удалить все макросы из чертежа Visio.
### **Пример программирования удаления всех макросов**
```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load a Visio diagram
diagram = Diagram("Macro.vsdm")

# remove all macros
diagram.setVbProjectData(None)

# Save diagram
diagram.save("RemoveMacrosFromVisio_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}
```
