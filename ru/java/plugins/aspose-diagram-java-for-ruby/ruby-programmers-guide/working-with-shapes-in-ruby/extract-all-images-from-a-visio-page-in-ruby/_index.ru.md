---
title: Извлечь все изображения со страницы Visio в Ruby
type: docs
weight: 30
url: /ru/java/extract-all-images-from-a-visio-page-in-ruby/
---
## **Aspose.Diagram — Извлечение всех изображений со страницы Visio**
 Чтобы извлечь все изображения со страницы Visio, используя**Aspose.Diagram Java для рубина** , просто вызовите**Извлечь изображения** модуль. Здесь вы можете увидеть пример кода.

**Рубиновый код**

{{< highlight "ruby" >}}

 данные_dir = File.dirname(File.dirname(File.dirname(File.dirname(__ФАЙЛ__)))) + '/данные/'

\# Создать экземпляр Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

формы = diagram.getPages().getPage("Поток 1").getShapes()

я = 0

 в то время как я< shapes.getCount()

    shape = shapes.get(i)

    # Filter shapes by type Foreign

    if shape.getType() == Rjb::import('com.aspose.diagram.TypeValue').FOREIGN

        # create an image file

        fos = Rjb::import('java.io.FileOutputStream').new(data_dir + "Image#{i}.bmp")

        fos.write(shape.getForeignData().getValue())

        fos.close()

    end

    i +=1

end

puts "Extracted images successfully!"

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Извлечь все изображения со страницы Visio (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/extractimages.rb)
