---
title: Повернуть фигуру на подходящий угол в Ruby
type: docs
weight: 80
url: /ru/java/rotate-a-shape-with-suitable-angle-in-ruby/
---
## **Aspose.Diagram - Повернуть фигуру на подходящий угол**
 Чтобы повернуть фигуру на подходящий угол, используя**Aspose.Diagram Java для рубина** , просто вызовите**Повернуть фигуру** модуль. Здесь вы можете увидеть пример кода.

**Рубиновый код**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Add a shape and set the angle

diagram.getPages().getPage(0).getShapes().getShape(1).setAngle(190)

\# Save diagram

diagram.save(data_dir + "RotateShape.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Rotated shape."

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Поворот фигуры на подходящий угол (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/rotateshape.rb)
