---
title: Настройте объекты формы со слоями в Visio в Ruby
type: docs
weight: 20
url: /ru/java/configure-shape-objects-with-layers-in-visio-in-ruby/
---
## **Aspose.Diagram - Настройка объектов формы со слоями**
 Чтобы настроить объекты формы со слоями, используя**Aspose.Diagram Java для рубина** , просто вызовите**Настроить шапевисслои** модуль. Здесь вы можете увидеть пример кода.

**Рубиновый код**

{{< highlight "ruby" >}}

 данные_dir = File.dirname(File.dirname(File.dirname(File.dirname(__ФАЙЛ__)))) + '/данные/'

\# Создать экземпляр Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

формы = diagram.getPages().getPage("Поток 1").getShapes()

я = 0

 в то время как я< shapes.getCount()

    shape = shapes.get(i)

    #puts shape.getName().to_s

    if shape.getName() == "Process"

        # Add shape1 in first two layers. Here "0;1" are indexes of the layers

        layer = shape.getLayerMem()

        layer.getLayerMember().setValue("0;1")

    elsif shape.getName() == "Preparation"

        # Remove shape2 from all the layers

        layer = shape.getLayerMem()

        layer.getLayerMember().setValue("")

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "Layers.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Configured Shape Objects with Layers in Visio."

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Настройте объекты формы со слоями в Visio (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Layers/configureshapewithlayers.rb)
