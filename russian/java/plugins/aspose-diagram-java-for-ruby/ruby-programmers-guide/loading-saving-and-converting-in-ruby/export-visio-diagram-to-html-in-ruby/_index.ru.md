---
title: Экспорт Visio Diagram в HTML на Ruby
type: docs
weight: 20
url: /ru/java/export-visio-diagram-to-html-in-ruby/
---
## **Aspose.Diagram - Экспорт Visio Diagram в HTML**
 Чтобы экспортировать Visio Diagram в HTML, используя**Aspose.Diagram Java для рубина** , просто вызовите**Экспорттохтмл** модуль. Здесь вы можете увидеть пример кода.

**Рубиновый код**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Save as Html

diagram.save(data_dir + "Diagram.html", Rjb::import('com.aspose.diagram.SaveFileFormat').HTML)

puts "Exported visio diagram to HTML."

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Экспорт Visio Diagram в HTML (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttohtml.rb)
