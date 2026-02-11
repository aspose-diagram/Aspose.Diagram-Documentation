---
title: Расчет значений выводов и установка размера формы
type: docs
weight: 60
url: /ru/net/calculate-pin-values-and-setting-size-of-a-shape/
description: В этом разделе объясняется, как рассчитать значения PinX и PinY подформы с помощью Aspose.Diagram.
---
## **Вычислите значения PinX и PinY вспомогательной формы**
 Если фигура является дочерним узлом групповой фигуры, ее xform является относительной координатой родительской фигуры, но не абсолютной координатой в[Страница](http://www.aspose.com/api/net/diagram/aspose.diagram/page). Если пользователю требуется получить абсолютную координату, этот пример кода поможет.

Точку, указанную в локальных координатах, можно преобразовать в родительские координаты, применив следующие преобразования в следующем порядке:

1. Вычтите значение свойства LocPinX элемента Cell_Type из координаты x.
1. Вычтите значение свойства LocPinY Cell_Type из координаты y.
1. Отразите точку относительно оси Y, если значение свойства FlipX Cell_Type равно единице.
1. Отразите точку относительно оси x, если значение свойства FlipY для Cell_Type равно единице.
1. Поверните точку против часовой стрелки вокруг начала координат на значение свойства Angle типа Cell_Type.
1. Добавьте значение PinX Cell_Type к координате x.
1. Добавьте значение PinY Cell_Type к координате y.
### **Вычислите пример программирования PinX и PinY**
Используйте следующий код в своем приложении .NET для вычисления значений PinX и PinY подфигуры с помощью Aspose.Diagram for .NET API.








{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get a group shape by ID and page index is 0
Shape shape = diagram.Pages[0].Shapes.GetShape(795);
// Get a sub-shape of the group shape by id
Shape subShape = shape.Shapes.GetShape(794);

Matrix m = new Matrix();
// Apply the translation vector
m.Translate(-(float)subShape.XForm.LocPinX.Value, -(float)subShape.XForm.LocPinY.Value);
// Set the elements of that matrix to a rotation
m.Rotate((float)subShape.XForm.Angle.Value);
// Apply the translation vector
m.Translate((float)subShape.XForm.PinX.Value, (float)subShape.XForm.PinY.Value);

// Get pinx and piny
double pinx = m.OffsetX;
double piny = m.OffsetY;
// Calculate the sub-shape pinx and piny
double resultx = shape.XForm.PinX.Value - shape.XForm.LocPinX.Value - pinx;
double resulty = shape.XForm.PinY.Value - shape.XForm.LocPinY.Value - piny;

{{< /highlight >}}

## **Установка высоты и ширины фигуры**
[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Класс позволяет управлять размером фигуры, указывая высоту и ширину фигуры с помощью методов SetHeight и SetWidth.

 Методы SetHeight и SetWidth, предоставляемые[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)class, поддержка изменения размера фигуры с мастером, без мастера или в виде групповой фигуры. Примеры кода в этой статье задают высоту и ширину для изменения размера фигуры на странице.

Процесс установки высоты и ширины:

1. Загрузите diagram.
1. Найдите определенную форму.
1. Установите высоту фигуры.
1. Установите ширину фигуры.
1. Сохраните номер diagram.
### **Пример программирования установки высоты и ширины**
Фрагмент кода ниже показывает, как установить высоту и ширину фигуры. Код ищет прямоугольник имени фигуры с идентификатором фигуры 1 и задает для его высоты и ширины значение double.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");
// Get shape by id
Shape shape = page.Shapes.GetShape(796);
// Alter the size of Shape
shape.SetWidth(2 * shape.XForm.Width.Value);
shape.SetHeight(2 * shape.XForm.Height.Value);
// Save diagram
diagram.Save(dataDir + "ChangeShapeSize_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

