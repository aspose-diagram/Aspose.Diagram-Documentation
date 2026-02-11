---
title: Расчет значений выводов и установка размера формы
type: docs
weight: 40
url: /ru/java/calculate-pin-values-and-setting-size-of-a-shape/
---
## **Вычислите значения PinX и PinY вспомогательной формы**
 Если фигура является дочерней фигурой группы, ее xform является относительной координатой родительской фигуры, но не абсолютной координатой в[Страница](https://reference.aspose.com/diagram/java/com.aspose.diagram/page). Если пользователю требуется получить абсолютную координату, этот пример кода поможет.

Точку, указанную в локальных координатах, можно преобразовать в родительские координаты, применив следующие преобразования в следующем порядке:

1. Вычтите значение свойства LocPinX элемента Cell_Type из координаты x.
1. Вычтите значение свойства LocPinY Cell_Type из координаты y.
1. Отразите точку относительно оси Y, если значение свойства FlipX Cell_Type равно единице.
1. Отразите точку относительно оси x, если значение свойства FlipY для Cell_Type равно единице.
1. Поверните точку против часовой стрелки вокруг начала координат на значение свойства Angle типа Cell_Type.
1. Добавьте значение PinX Cell_Type к координате x.
1. Добавьте значение PinY Cell_Type к координате y.
### **Вычислите пример программирования PinX и PinY**
Используйте следующий код в своем приложении Java для вычисления значений PinX и PinY подфигуры с помощью Aspose.Diagram for Java API.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CalculateCenterOfSubShapes.class);
        
// load Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get group shape
Shape shape = diagram.getPages().get(0).getShapes().getShape(138);
// get sub-shape of the group shape
Shape subShape = shape.getShapes().getShape(140);


AffineTransform m = new AffineTransform();
// apply the translation vector
m.translate(-(float)subShape.getXForm().getLocPinX().getValue(), -(float)subShape.getXForm().getLocPinY().getValue());		
// set the elements of that matrix to a rotation
m.rotate((float)subShape.getXForm().getAngle().getValue());
// apply the translation vector
m.translate((float)subShape.getXForm().getPinX().getValue(), (float)subShape.getXForm().getPinY().getValue());

// get pinx and piny		
double pinx = m.getTranslateX();
double piny = m.getTranslateY();
		
// calculate the sub-shape pinx and piny
double resultx = shape.getXForm().getPinX().getValue() - shape.getXForm().getLocPinX().getValue() - pinx;
double resulty = shape.getXForm().getPinY().getValue() - shape.getXForm().getLocPinY().getValue() - piny;

{{< /highlight >}}
```
## **Установка высоты и ширины фигуры**
[Форма](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) Класс позволяет управлять размером фигуры, указывая высоту и ширину фигуры с помощью методов SetHeight и SetWidth.

 Методы SetHeight и SetWidth, предоставляемые[Форма](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape)class, поддержка изменения размера фигуры с мастером, без мастера или в виде групповой фигуры.

Примеры кода в этой статье задают высоту и ширину для изменения размера фигуры на странице.

**Ввод diagram** 

![дело:изображение_альтернативный_текст](http://i.imgur.com/cTiNWa7.png)

**diagram после изменения высоты и ширины**

![дело:изображение_альтернативный_текст](calculate-pin-values-and-setting-size-of-a-shape_1.png)

Процесс установки высоты и ширины:

1. Загрузите diagram.
1. Найдите определенную форму.
1. Установите высоту фигуры.
1. Установите ширину фигуры.
1. Сохраните номер diagram.
### **Пример программирования установки высоты и ширины**
Фрагмент кода ниже показывает, как установить высоту и ширину фигуры. Код ищет прямоугольник имени фигуры с идентификатором фигуры 1 и задает для его высоты и ширины значение double.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ChangeShapeSize.class);
        
// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");
// get shape by id
Shape shape = page.getShapes().getShape(796);
// alter the size of Shape
shape.setWidth(2 * shape.getXForm().getWidth().getValue());
shape.setHeight(2 * shape.getXForm().getHeight().getValue());
// save diagram
diagram.save(dataDir + "ChangeShapeSize_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
