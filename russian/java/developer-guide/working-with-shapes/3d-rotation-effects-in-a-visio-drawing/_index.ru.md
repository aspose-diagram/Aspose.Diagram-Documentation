---
title: 3D-эффекты вращения в чертеже Visio
type: docs
weight: 90
url: /ru/java/3d-rotation-effects-in-a-visio-drawing/
---
## **Задайте свойства вращения 3D в Shapesheet**
Aspose.Diagram for Java API позволяет разработчикам изменять значения поворота 3D в таблице форм. Значения ячеек RotationXAngle, RotationYAngle и RotationZAngle контролируют угол поворота по каждой из соответствующих осей. Значение перечисления RotationType управляет типом вращения:

1. Параллельное вращение, при котором фигура поворачивается без учета линейной перспективы.
1. Перспективное вращение, при котором фигура поворачивается с линейной перспективой.
1. Предустановки наклонного вращения (внизу слева, внизу справа, вверху слева и вверху справа), где фигура поворачивается с наклонной проекцией.

**KeepTextFlat**значение ячейки указывает, будет ли текст фигуры игнорировать вращение фигуры в 3-D. Это не относится к двумерному вращению.**РасстояниеОт Земли**значение ячейки определяет расстояние, на которое объект поднимается от земли в точках при вращении в 3-D.**Перспектива**значение ячейки определяет угол перспективы для перспективного поворота в градусах (от 0 до 359,9).
### **Установка свойств поворота 3D**
Член ThreeDFormat, предоставленный[Форма](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape)можно использовать для установки свойств вращения 3D.

В приведенном ниже коде показано, как:

1. Загрузите исходный чертеж.
1. Получить фигуру по имени страницы и параметрам идентификатора.
1. Задайте свойства трехмерного вращения.
1. Сохранить рисунок
#### **Пример программирования трехмерного вращения**
Используйте следующий код в своем приложении Java, чтобы установить свойства трехмерного вращения с помощью Aspose.Diagram for Java API.

**Java**

{{< highlight "java" >}}

 // load diagram

Diagram diagram = new Diagram("c:\\temp\\TestTemplate.vsdx");

// get shape by ID and page name

Shape shape = diagram.getPages().getPage("Page-1").getShapes().getShape(0);



// set 3D rotation properties

shape.getThreeDFormat().getRotationXAngle().setValue(2.61);

shape.getThreeDFormat().getRotationYAngle().setValue(2.61);

shape.getThreeDFormat().getRotationZAngle().setValue(3);

shape.getThreeDFormat().getRotationType().setValue(RotationTypeValue.PARALLEL);

shape.getThreeDFormat().getPerspective().setValue(0);

shape.getThreeDFormat().getDistanceFromGround().setValue(0);

shape.getThreeDFormat().getKeepTextFlat().setValue(BOOL.TRUE);

// save drawing

diagram.save("c:\\temp\\TestTemplate.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
