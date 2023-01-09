---
title: 3D-эффекты вращения в чертеже Visio
type: docs
weight: 90
url: /ru/net/3d-rotation-effects-in-a-visio-drawing/
description: В этом разделе объясняется, как установить свойства вращения 3D в Shapesheet с помощью Aspose.Diagram.
---
## **Задайте свойства вращения 3D в Shapesheet**
Aspose.Diagram API позволяет разработчикам изменять значения поворота 3D в таблице форм. Значения ячеек RotationXAngle, RotationYAngle и RotationZAngle контролируют угол поворота по каждой из соответствующих осей. Значение перечисления RotationType управляет типом вращения:

1. Параллельное вращение, при котором фигура поворачивается без учета линейной перспективы.
1. Перспективное вращение, при котором фигура поворачивается с линейной перспективой.
1. Предустановки наклонного вращения (внизу слева, внизу справа, вверху слева и вверху справа), где фигура поворачивается с наклонной проекцией.

**KeepTextFlat** значение ячейки указывает, будет ли текст фигуры игнорировать вращение фигуры в 3-D. Это не относится к двумерному вращению.**РасстояниеОт Земли** значение ячейки определяет расстояние, на которое объект поднимается от земли в точках при вращении в 3-D.**Перспектива** значение ячейки определяет угол перспективы для перспективного поворота в градусах (от 0 до 359,9).
### **Установка свойств поворота 3D**
 Член ThreeDFormat, предоставленный[Форма](https://reference.aspose.com/diagram/net/aspose.diagram/shape)можно использовать для установки свойств вращения 3D.

В приведенном ниже коде показано, как:

1. Загрузите исходный чертеж.
1. Получить фигуру по имени страницы и параметрам идентификатора.
1. Задайте свойства трехмерного вращения.
1. Сохранить рисунок
#### **Пример программирования трехмерного вращения**
Используйте следующий код в своем приложении .NET, чтобы установить свойства трехмерного вращения с помощью Aspose.Diagram for .NET API.

**.NET, C#**

{{< highlight "java" >}}

 // load diagram

Diagram diagram = new Diagram(@"c:\temp\TestTemplate.vsdx");

// get shape by ID and page name

Shape shape = diagram.Pages.GetPage("Page-1").Shapes.GetShape(0);



// set 3D rotation properties

shape.ThreeDFormat.RotationXAngle.Value = 2.61;

shape.ThreeDFormat.RotationYAngle.Value = 2.61;

shape.ThreeDFormat.RotationZAngle.Value = 3;

shape.ThreeDFormat.RotationType.Value = RotationTypeValue.ObliqueFromBottomLeft;

shape.ThreeDFormat.Perspective.Value = 0;

shape.ThreeDFormat.DistanceFromGround.Value = 0;

shape.ThreeDFormat.KeepTextFlat.Value = BOOL.True;

// save drawing

diagram.Save(@"c:\temp\TestTemplate.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
