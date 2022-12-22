---
title: Экспорт Visio Diagram в PDF в Ruby
type: docs
weight: 40
url: /ru/java/export-visio-diagram-to-pdf-in-ruby/
---
## **Aspose.Diagram - Экспорт Visio Diagram в PDF**
 Чтобы экспортировать Visio Diagram в PDF, используя**Aspose.Diagram Java для рубина** , просто вызовите**Экспорт в PDF** модуль. Здесь вы можете увидеть пример кода.

**Рубиновый код**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Save as PDF file format

diagram.save(data_dir + "Diagram.pdf", Rjb::import('com.aspose.diagram.SaveFileFormat').PDF)

puts "Exported visio diagram to pdf."

{{< /highlight >}}
## **Скачать рабочий код**
Скачать**Экспорт Visio Diagram в PDF (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttopdf.rb)
