---
title: Обновление Visio Текст формы в Ruby
type: docs
weight: 30
url: /ru/java/update-visio-shape-text-in-ruby/
---
## **Aspose.Diagram — Обновление Visio Текст формы**
Чтобы обновить текст формы Visio, используя**Aspose.Diagram Java для рубина** , просто вызовите**ОбновитьShapeText** модуль. Здесь вы можете увидеть пример кода.

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

        shape.getText().getValue().clear()

        shape.getText().getValue().add(Rjb::import('com.aspose.diagram.Txt').new("New Text"))

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "UpdateShapeText.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Updated shape text."

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Обновление Visio Текст формы (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Text/updateshapetext.rb)
