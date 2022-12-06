---
title: Получить Visio информацию о форме в Ruby
type: docs
weight: 70
url: /ru/java/retrieve-visio-shape-information-in-ruby/
---
## **Aspose.Diagram — Получить информацию о форме Visio**
 Чтобы получить информацию о форме Visio, используя**Aspose.Diagram Java для рубина** , просто вызовите**GetShapeInfo** модуль. Здесь вы можете увидеть пример кода.

**Рубиновый код**

{{< highlight "ruby" >}}

 данные_dir = File.dirname(File.dirname(File.dirname(File.dirname(__ФАЙЛ__)))) + '/данные/'

\# Создать экземпляр Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

формы = diagram.getPages().getPage(0).getShapes()

я = 0

 в то время как я< shapes.getCount()

    shape = shapes.get(i)

    # Display information about the shapes

    puts "Shape ID : " + shape.getID().to_s

    puts "Name : " + shape.getName().to_s

    puts "Master Shape : " + shape.getMaster().getName().to_s

    i +=1

end

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Получить информацию о форме Visio (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/getshapeinfo.rb)
