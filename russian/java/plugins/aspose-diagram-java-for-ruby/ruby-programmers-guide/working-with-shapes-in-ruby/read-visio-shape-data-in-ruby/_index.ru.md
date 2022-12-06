---
title: Чтение данных формы Visio в Ruby
type: docs
weight: 50
url: /ru/java/read-visio-shape-data-in-ruby/
---
## **Aspose.Diagram — Чтение всех свойств формы**
 Чтобы прочитать все свойства формы, используя**Aspose.Diagram Java для рубина** , вызов**read_all_shape_properties** метод**Риадшапедата** модуль. Здесь вы можете увидеть пример кода.

**Рубиновый код**

{{< highlight "ruby" >}}

 деф читать_все_shape_properties()

 данные_dir = File.dirname(File.dirname(File.dirname(File.dirname(__ФАЙЛ__)))) + '/данные/'

 # Создать экземпляр Diagram

 diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

 формы = diagram.getPages().getPage(0).getShapes()



 я = 0

 в то время как я< shapes.getCount()

        shape = shapes.get(i)

        if shape.getName() == "Process"

            j = 0

            while j < shape.getProps().getCount()

                property = shape.getProps().get(j)

                puts property.getLabel().getValue() + ": " + property.getValue().getVal()

                j +=1

            end

            break

        end

        i +=1

    end

end

{{< /highlight >}}
## **Aspose.Diagram — Чтение свойства формы по имени**
 Чтобы прочитать свойство формы по имени, используя**Aspose.Diagram Java для рубина** , вызов**read_shape_property_by_name** метод**Риадшапедата** модуль. Здесь вы можете увидеть пример кода.

**Рубиновый код**

{{< highlight "ruby" >}}

 деф читать_форма_имущество_по_имя()

 данные_dir = File.dirname(File.dirname(File.dirname(File.dirname(__ФАЙЛ__)))) + '/данные/'

 # Создать экземпляр Diagram

 diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

 формы = diagram.getPages().getPage(0).getShapes()



 я = 0

 в то время как я< shapes.getCount()

        shape = shapes.get(i)

        if shape.getName() == "Process"

            property = shape.getProps().getProp("Cost")

            puts property.getLabel().getValue() + ": " + property.getValue().getVal()

        end

        i +=1

    end

end

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Чтение данных формы Visio (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/readshapedata.rb)
