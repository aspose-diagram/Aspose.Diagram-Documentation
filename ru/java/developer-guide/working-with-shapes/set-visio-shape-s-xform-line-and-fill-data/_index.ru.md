---
title: Установите Visio XForm, линии и данные заливки фигуры
type: docs
weight: 70
url: /ru/java/set-visio-shape-s-xform-line-and-fill-data/
---
## **Настройка данных XForm**
 Элемент XForm является частью схемы XML Microsoft Visio. XForm указывает положение фигуры, например ширину, высоту, поворот и была ли фигура перевернута.[XForm](https://reference.aspose.com/diagram/java/com.aspose.diagram/xform) имущество, выставленное[Форма](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class поддерживает объект Aspose.Diagram.XForm. Свойство XForm можно использовать для извлечения или обновления данных XForm фигуры. Примеры кода в этой статье изменяют значения XForm PinX (координата X) и PinY (координата Y) для перемещения фигур на странице.

**Ввод diagram** 

![дело:изображение_альтернативный_текст](set-visio-shape-s-xform-line-and-fill-data_1.png)

**diagram после** **PinX** **а также** **PinY** **значения были изменены** 

![дело:изображение_альтернативный_текст](set-visio-shape-s-xform-line-and-fill-data_2.png)

Процесс обновления данных XForm:

1. Загрузите diagram.# Найдите конкретную фигуру.# Обновите данные XForm фигуры.
1. Сохраните номер diagram.
### **Образец программирования**
Фрагмент кода ниже показывает, как обновить данные XForm фигуры. Код ищет процесс имен фигур с идентификатором фигуры 1 и устанавливает его координаты X и Y равными 5.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetXFormdata.class); 
// call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "SetXFormdata.vsd");

//Find a particular shape and update its XForm
for(Shape shape :(Iterable<Shape>) diagram.getPages().get(0).getShapes())
{
    if (shape.getNameU().toLowerCase() == "process" && shape.getID() == 1)
    {
        shape.getXForm().getPinX().setValue(5);
        shape.getXForm().getPinY().setValue(5);
    }
}
// save diagram
diagram.save(dataDir + "SetXFormdata_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Установить Visio данные линии фигуры**
Формы можно форматировать несколькими способами. В этой статье показано, как указать атрибуты линии.

Microsoft Visio позволяет пользователям форматировать строки различными способами. Aspose.Diagram for Java поддерживает:

- Вес: толщина линии.
- Цвет: установите цвет линии фигуры.
- Прозрачность цвета линии: установите прозрачность цвета линии фигуры в процентах.
- Узор: определяет, является ли линия сплошной, пунктирной или имеет другой узор.
- Скругление: радиус углов.
- Начальная и конечная стрелки: указано, есть ли в строке стрелки.
- Начальный и конечный размеры стрелок: задайте размеры стрелок.
- Заглушка: закругление линии заканчивается.
### **Измените цвет линии, толщину, тип штриха, прозрачность, округление, тип стрелки и размер стрелки границы фигуры.**
[Линия](https://reference.aspose.com/diagram/java/com.aspose.diagram/line) имущество, выставленное[Форма](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)class, поддерживает объект Aspose.Diagram.Line. Это свойство можно использовать для извлечения или обновления данных линии фигуры.
#### **Образец программирования линейных данных**
Следующий фрагмент кода обновляет линейные данные shape.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetLineData.class);

// load a Visio diagram
Diagram diagram = new Diagram(dataDir + "SetLineData.vsd");
// get the page by its name
Page page1 = diagram.getPages().getPage("Page-1");
// get shape by its ID
Shape shape = page1.getShapes().getShape(1);
// set line dash type by index
shape.getLine().getLinePattern().setValue(4);
// set line weight, defualt in PT
shape.getLine().getLineWeight().setValue(2);
// set color of the shape's line
shape.getLine().getLineColor().getUfe().setF("RGB(95,108,53)");
// set line rounding, default in inch
shape.getLine().getRounding().setValue(0.3125);
// set line caps
shape.getLine().getLineCap().setValue(BOOL.TRUE);
// set line color transparency in percent
shape.getLine().getLineColorTrans().setValue(50);

/* add arrows to the connector or curve shapes */
// select arrow type by index
shape.getLine().getBeginArrow().setValue(4);
shape.getLine().getEndArrow().setValue(4);
// set arrow size 
shape.getLine().getBeginArrowSize().setValue(ArrowSizeValue.LARGE);
shape.getLine().getBeginArrowSize().setValue(ArrowSizeValue.LARGE);

// save the Visio
diagram.save(dataDir + "SetLineData_Out.vsdx", SaveFileFormat.VSDX);
// save diagram
diagram.save(dataDir+ "output.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
## **Установить Visio данные заполнения фигуры**
Формы можно форматировать несколькими способами. В этом разделе описывается, как задать заливку фигуры.

 Microsoft Office Visio позволяет пользователям форматировать заливки различными способами.[Наполнять](https://reference.aspose.com/diagram/java/com.aspose.diagram/fill) класс Aspose.Diagram for Java API поддерживает настройку:

- Цвета фона и переднего плана.
- Прозрачность.
- Заполнение узорами.
- Тени.
### **Установка значений заполнения**
Свойство Fill, предоставляемое классом Shape, поддерживает объект Aspose.Diagram.Fill. Свойство Fill можно использовать для извлечения или обновления данных заполнения фигуры.

|<p>**Ввод diagram** </p><p>![дело:изображение_альтернативный_текст](http://i.imgur.com/OrhEecb.png)</p>|<p>**diagram после изменения цвета заливки** </p><p>![дело:изображение_альтернативный_текст](http://i.imgur.com/HO0wmZ8.png)</p>|
|:- |:- |
#### **Образец программирования данных заполнения**
Следующий фрагмент кода обновляет данные заполнения фигуры. Код ищет фигуру с именем прямоугольник с идентификатором фигуры 1 и устанавливает цвета фона и переднего плана заливки.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetFillData.class);


//Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir+ "Drawing1.vsd");

//Find a particular shape and update its XForm
for (com.aspose.diagram.Shape shape : (Iterable<Shape>) diagram.getPages().get(0).getShapes())
{
    if (shape.getNameU().toLowerCase() == "rectangle" && shape.getID() == 1)
    {
        shape.getFill().getFillBkgnd().setValue(diagram.getPages().getPage(0).getShapes().getShape(0).getFill().getFillBkgnd().getValue());
        shape.getFill().getFillForegnd().setValue("#ebf8df");
    }
}
// save diagram
diagram.save(dataDir+ "SetFillData_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
### **Получить унаследованные данные заполнения формы Visio**
Фигуры Visio могут наследовать родительский стиль и основную фигуру. Разработчики могут получить или установить наследуемые данные заполнения фигуры Visio. Свойство InheritFill, предоставляемое классом Shape, содержит значения форматирования заливки для фигуры, наследуемой родительским стилем и основной фигурой.
#### **Пример программирования извлечения унаследованных данных заполнения**
Следующий фрагмент кода извлекает унаследованные данные заливки фигуры. Пожалуйста, проверьте этот пример кода:

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveInheritedFillData.class) + "Shapes/";

// Call the diagram constructor to load a VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get page by ID
Page page = diagram.getPages().getPage("Page-1");
// Get shape by ID
Shape shape = page.getShapes().getShape(1);
// Get the fill formatting values
System.out.println(shape.getInheritFill().getFillBkgnd().getValue());
System.out.println(shape.getInheritFill().getFillForegnd().getValue());
System.out.println(shape.getInheritFill().getFillPattern().getValue());
System.out.println(shape.getInheritFill().getShapeShdwObliqueAngle().getValue());
System.out.println(shape.getInheritFill().getShapeShdwOffsetX().getValue());
System.out.println(shape.getInheritFill().getShapeShdwOffsetY().getValue());
System.out.println(shape.getInheritFill().getShapeShdwScaleFactor().getValue());
System.out.println(shape.getInheritFill().getShapeShdwType().getValue());
System.out.println(shape.getInheritFill().getShdwBkgnd().getValue());
System.out.println(shape.getInheritFill().getShdwBkgndTrans().getValue());
System.out.println(shape.getInheritFill().getShdwForegnd().getValue());
System.out.println(shape.getInheritFill().getShdwForegndTrans().getValue());
System.out.println(shape.getInheritFill().getShdwPattern().getValue());

{{< /highlight >}}
```
