---
title: Установить Visio данные линии формы в Ruby
type: docs
weight: 140
url: /ru/java/set-visio-shape-s-line-data-in-ruby/
---
## **Aspose.Diagram - Установить Visio данные линии фигуры**
 Чтобы установить данные линии формы Visio, используя**Aspose.Diagram Java для рубина** , просто вызовите**СетШапеЛайнДата** модуль. Здесь вы можете увидеть пример кода.

**Рубиновый код**

{{< highlight "ruby" >}}

 данные_dir = File.dirname(File.dirname(File.dirname(File.dirname(__ФАЙЛ__)))) + '/данные/'

\# Создать экземпляр Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

формы = diagram.getPages().getPage(0).getShapes()

я = 0

 в то время как я< shapes.getCount()

    shape = shapes.get(i)

    if shape.getNameU() == "rectangle" && shape.getID() == 1

        shape.getLine().getLineColor().setValue(diagram.getPages().getPage(0).getShapes().getShape(1).getFill().getFillForegnd().getValue())

        shape.getLine().getLineWeight().setValue(0.07041666666666667)

        shape.getLine().getRounding().setValue(0.1)

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "SetShapeLineData.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Set visio shape's line data."

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Установить Visio данные линии формы (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/setshapelinedata.rb)
