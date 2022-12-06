---
title: Изменить положение фигуры в Ruby
type: docs
weight: 10
url: /ru/java/change-the-position-of-a-shape-in-ruby/
---
## **Aspose.Diagram - Изменить положение фигуры**
 Чтобы изменить положение фигуры с помощью**Aspose.Diagram Java для рубина** , просто вызовите**ИзменитьШапеПоситион** модуль. Здесь вы можете увидеть пример кода.

**Рубиновый код**

{{< highlight "ruby" >}}

 данные_dir = File.dirname(File.dirname(File.dirname(File.dirname(__ФАЙЛ__)))) + '/данные/'

\# Создать экземпляр Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

формы = diagram.getPages().getPage(0).getShapes()

я = 0

 в то время как я< shapes.getCount()

    shape = shapes.get(i)

    if shape.getNameU() == "Process" && shape.getID() == 2

        shape.move(1, 1)

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "ChangeShapePosition.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Changed position of a shape."

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Изменение положения фигуры (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/changeshapeposition.rb)
