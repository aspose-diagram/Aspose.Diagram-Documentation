---
title: Экспорт Visio Diagram в изображение в Ruby
type: docs
weight: 30
url: /ru/java/export-visio-diagram-to-image-in-ruby/
---
## **Aspose.Diagram - Экспорт Visio Diagram в изображение**
 Чтобы экспортировать Visio Diagram в изображение, используя**Aspose.Diagram Java для рубина** , просто вызовите**Экспорт в изображение** модуль. Здесь вы можете увидеть пример кода.

**Рубиновый код**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Save as PNG

diagram.save(data_dir + "Diagram.png", Rjb::import('com.aspose.diagram.SaveFileFormat').PNG)

puts "Exported visio diagram to PNG."

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Экспорт Visio Diagram в изображение (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttoimage.rb)
