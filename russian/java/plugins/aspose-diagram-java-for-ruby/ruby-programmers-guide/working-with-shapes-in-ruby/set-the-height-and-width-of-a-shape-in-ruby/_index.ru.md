---
title: Установите высоту и ширину фигуры в Ruby
type: docs
weight: 120
url: /ru/java/set-the-height-and-width-of-a-shape-in-ruby/
---
## **Aspose.Diagram - Установка высоты и ширины фигуры**
 Чтобы установить высоту и ширину фигуры с помощью**Aspose.Diagram Java для рубина** , просто вызовите**SetShapeHeightAndWidth** модуль. Здесь вы можете увидеть пример кода.

**Рубиновый код**

{{< highlight "ruby" >}}

 данные_dir = File.dirname(File.dirname(File.dirname(File.dirname(__ФАЙЛ__)))) + '/данные/'

\# Создать экземпляр Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

формы = diagram.getPages().getPage(0).getShapes()

я = 0

 в то время как я< shapes.getCount()

    shape = shapes.get(i)

    if shape.getNameU() == "Process" && shape.getID() == 1

        shape.setWidth(2 * shape.getXForm().getWidth().getValue())

        shape.setHeight(2 * shape.getXForm().getHeight().getValue())

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "SetShapeHeightAndWidth.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Set height and width of shape."

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Установка высоты и ширины фигуры (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/setshapeheightandwidth.rb)
